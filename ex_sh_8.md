# Ex. 1 - DOs and DON’Ts of Code and Connections

## a) Secure connections should be encrypted, authenticated and tamper-proof. Explain why and how this is achieved.


Why:

- Encrypted: sent messages can only be read at communicating endpoints
- Authenticated: both endpoints know for sure that they are communicating with the right counterparts
- Tamper-proof: Integrity checks assure that messages are received the way they were sent

We need secure conections because when dealing with sensitive data we need to have everyone authenticated with no other third party being able to read or alter the messages. 

## b) Name some problems that can occur when sanitizing data.

We might forget to sanitize data.
Data might be sanitized the wrong way.
Don't create your own sanitization method.
Sanitize characters.
Saniteze the right data the right way.

## c) Why is sanitization of debug / logging output important as well?

To anonimize users and not leak user data. If the data is stored in a not so secure server or returned in an error message that could lead to direct harm to users or the company if it gest leaked.

# Ex. 2 - Cryptography

## a) Explain how a symmetric encryption works.

Both parties have the same cryptographic key.

## b) Explain how an asymmetric encryption works.

One party has a private key, that can be used to sign or to decrypt a message.

Another has a public key, that can be used to verify a signature of to encrypt a message.

## c) Compare stream cipher with block ciphers.

Stream cypher the key is turned into a key and the plaintext is converted to ciphertext by xor-ing with the key.

Block cipher the message is split into to blocks and each block is encripted, can be paralelized, but corelations can be made with the encripted blocks.

# Ex. 3 - Message Authentication Codes (MAC) and Signatures

[//]: # (Change the order of the questions)


[//]: # (Not really specified in the slides)
## a) What are MACs used for and how do they work?

MACs are a guarantee that a given sender wrote a message, there will be a code that can be used by the reciever to validade the message using a specific algorithm and key.

The most secure way to is to encript a message and then run it through the MAC algorithm to ensure that both the ciphertext and the original text are intact.

[//]: # (Not really specified in the slides)
## b) What are signatures used for and how do they work?

Signatures are used to prove that a given entity has writen a given artifact. I works by hashing the artifact and then encripting that hash, it can then be sent with the arifact so that anyone with the decription key can see that the artifact was not altered.

## c) What are the differrences?




# Ex. 4 - RTFM

In the lecture, two papers were cited on why no one reads the manual. Answer the following sub-tasks:

## a) What are common alternatives to reading the manual that users used?

Look it up on google, a llm, forum, videos, asking someone or just trial and error.

## b) Why were manuals not used?

Hard to read, not made for the target audience, too many specific details.

Too many functionalities and congnitive orverload.

## c) What makes a good manual?

Short, with good examples, esily searchable, using sane defaults.

# Ex. 5 - Vulnerability of the Day - Hard-coded credentials and unsalted hashes



Fur diese Prasentation. Ich habe zwei Personen interviewt. Zuerst John, er studiert Informatik in dem Universitat Bonn. Er is im deine ersten Mastersemester. Und als ich ihn fragte wie er zum Uni kommt, er habt beantworted dass wenn das Wetter gut ist, er fahrt mit dem Fahrrad. Sonst er nehmt den Bus. Der zweite Personen, die ich interviewt habe, ist Jonas. Er auch studiert in das Universitat Bonn, und er studiert Computer Science, er ist auch im deine ersten Mastersemester. Jonas fahrt meistens mit dem fahrrad zur Universitat, und manchmal zu Fuß

- Ich heiße Jonas
- ⁠Ich studiere Computer Science an der Universität Bonn
- ⁠Ich wohne in Bonn
- ⁠Meistens fahre ich mit dem Fahrrad zur Universität, manchmal auch zu Fuß
- Unter nachhaltigen Verkehr verstehe ich unter anderem mehr Busse und Züge, als auch mehr und breitere Fahrradwege
- ⁠Ja, ich benutze alle 3 Verkehrsmittel sehr häufig. Mit dem Deutschland-/Semesterticket komme ich so am schnellsten und günstigsten von A nach B
- Nachhaltiger Verkehr ist wichtig, weil er den Ausstoß von Treibhausgasen und Schadstoffen reduziert und so Klima, Luftqualität und Gesundheit schützt.



Hallo, mein Name ist John. 

Ich studiere Informatik im ersten Mastersemester.

Aktuell wohne ich in Bonn in NRW. 

Wenn das Wetter gut ist, fahre ich mit dem Fahrrad. Sonst nehme ich den Bus.

Für mich bedeuetet nachhaltiger Verkehr, dass alle Verkehrsgruppen (Autofahrer, Fahrradfahrer ... etc. ) gleichberechtigt am Verkehr teilnehmen können. Damit meine ich, dass  Städte und Orte sich nicht ausschließlich darauf konzentrieren sollten, dass Autofahrer gut durch die Stadt kommen, sondern auch Menschen mit der Bahn oder dem Fahrrad gute Verkehrsanbindungen zur Verfügung gestellt bekommen. 

Ja ich nutze oft den öffentlichen Nahverkehr. Nach meiner Meinung ist der öffentliche Nahverkehr besser, schneller und effizienter in der Stadt, als das Auto zu nutzen. 

Nachhaltiger Verkehr ist eichtig für die Umwelt, weil er mehr Menschen dazu bewegen kann, keine Diesel- oder Benzinautos zu verwenden, was die CO2-Emissionen verringert. Damit wird auch der Lärm und die Luftverschmutzung in den Orten reduziert. Gleichzeitig wird auch der Verkehr auf den Straßen weniger, was für weniger Staus und Frust bei Menschen sorgt.