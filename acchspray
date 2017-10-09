import tweepy


def get_api (jbw):
    auth = tweepy.OAuthHandler(jbw['consumer_key'], jbw['consumer_secret'])
    auth.set_access_token(jbw['access_token'], jbw['access_token_secret'])
    return tweepy.API(auth)


def main():
    jbw ={
    "consumer_key" : "consumer_key",
    "consumer_secret" : "consumer_secret",
    "access_token" : "access_token",
    "access_token_secret" : "access_token_secret"
    }

    api= get_api(acchspray)
    posted = True
    num = -1
    with open('C:\py\pray.txt', 'r+') as txt:
        while (posted):
            context = txt.readline()
            num += 1
            if "haveposted" in context:
                continue
            if "unposted" in context:
                lines = []
                file = open('C:\py\pray.txt', 'r')
                for line in file:
                    lines.append(line)
                file.close()
                lines.insert(num, "haveposted")
                s = ''.join(lines)
                f = open('C:\py\pray.txt', 'w+')
                f.write(s)
                f.close()
                del lines[:]
                final = context.replace("unposted", "")
                context = txt.readline()
                final = final + context
                num += 1
                posted = False

    final = "this is a auto pray program test\n" + final
    if final.__len__()<=140:
        api.update_status(status=final)
    else:
        print("failed")


if __name__ == "__main__":
  main()
