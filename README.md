# share-via
Share via Whatsapp, Linkedin, Twitter, etc for your web app and browser in mobile: 

## Linkedin
              <a onClick={() => window.open(`https://www.linkedin.com/shareArticle?mini=true&url=${shareUrl}`, '_blank')} size="lg:md"                                    variant="default" />
             
## Whatsapp
              <a onClick={() => window.open(`https://web.whatsapp.com/send?text=${shareUrl}`, '_blank')} size="lg:md" variant="default"/>
              
              # Whatsapp Mobile
              <a href={`https://wa.me/?text=${shareUrl}`} size="sm" variant="default" />
              
## Twitter
              <a onClick={() => window.open(`https://twitter.com/intent/tweet?text=${shareUrl}`, '_blank')} size="lg:md" variant="default"/>
              
              # Via Mail (I only added a body. You can add subject and the recepient(s) in addition to that)
              <a onClick={() => window.open(`mailto:?&body=${shareUrl}`, '_blank')} size="lg:md" variant="default" />
              
## Copy to clipboard
              <Button
                onClick={() =>
                  window.navigator.clipboard
                    .writeText(shareUrl)
                    .then(() => {
                      addToast({ message: 'copied to clipboard' });
                    })
                    .catch(() => {})
                }
                size="lg:md"
                variant="default"
              />
