# Weekly Scripting Challenge Recap Week: #6

Just because you `deactivate` a _Business Rule_, that does not mean it will automatically
kill an in process _Business Rule_ that is already runnung

**Best Practice when setting up integrations**
1. set up service account per integration
- Check with a client, may need a license
  - what is 1 license out of thousands
- If your integration breaks or won't stop running, kill the credentials and
  they won't have access to the system any longer


**External Communication Channels (ECC)**
Anytime you have anything interfacing with SNOW, it goes through the ECC queues
- Usually see `Heartbeat Probes` (millions)
  - Can filter this out

When working with other `parties` or `clients`, sometimes you have to work
with someone else that is working with the same mutual client
- sometimes need to have a sn rep work with their 3rd-party rep
- sometimes need to have a custom API created for us to consume their work



**CHALLENGE FOR NEXT WEEK**
- use rest message for giphy we just created
- make a UI action on an incident that when you click it, it will take the short description
  and search giphy for a randoms ticker based on whatever is in the short description, and
- redirect the user in a new tab to that gif


will have to dig into the JSON, and pull out the attribute (4 or 5 layers deep)
