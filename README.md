# 1. The Storage and Protection Element of ERA

I imagine that as long as I can store bytes, I can participate in this protocol. Storing bytes isn’t the hard part; coordinating their storage in a censorship-resistant manner is the challenge. Filecoin helps by combining cryptographic proofs with blockchain-based incentives, but I think ERA should be independent of the Filecoin network rather than dependent on it.

The question is: how can you have a protection element (i.e., ensuring that data is not tampered with and is censorship resistant) that is also agnostic to the method of storage (i.e., I can use Filecoin, Cloudflare, etc.)?

One solution is to publish the accepted hash of a document (similar to a checksum for downloaded files). These hashes can be uploaded to multiple blockchain layers for redundancy and easy querying and can be issued by the WEDF (which would act like a DAO). If we decouple the protection element from the storage, then anyone with their own storage provider can copy the data—as long as they can reproduce the checksum, they become a valid participant in the ERA protocol. (By the way, Filecoin tightly couples the protection and storage elements, which is why it uses a protocol called Proof of Spacetime (PoSt).)

I have explained how the system can be tamper resistant and storage-agnostic, but I haven’t yet addressed how it can be censorship resistant (I am building up to that).

---

# 2. The Collection and Structuring Element of ERA

This is the more theoretically sound part of the architecture because it standardizes “human rights” data so that it can be interoperable. A similar question was asked by Tim Berners-Lee, and his answer was “Web3”—not the crypto or blockchain version of Web3, but a vision of Web3 that existed before crypto and blockchains, known as the Semantic Web. (I simply copy-pasted the Wikipedia definition to get an idea.)

The Semantic Web, sometimes known as Web 3.0 (not to be confused with [Web3](https://en.wikipedia.org/wiki/Web3 "Web3")), is an extension of the [World Wide Web](https://en.wikipedia.org/wiki/World_Wide_Web "World Wide Web") through standards set by the [World Wide Web Consortium](https://en.wikipedia.org/wiki/World_Wide_Web_Consortium "World Wide Web Consortium") (W3C). Its goal is to make Internet data [machine-readable](https://en.wikipedia.org/wiki/Machine-readable "Machine-readable").

Semantic standards like OWL (Web Ontology Language) and CIDOC-CRM (Conceptual Reference Model) enable cross-domain data linking—or one can consider models like the Solid Pod. However, not all data is in this format, and converting data to this standard—or waiting for it to be converted—is not ideal. Therefore, I imagine ERA should still operate even if the data is in a simple format like a `.txt` file, although there is an incentive to adopt the standardized model.

Again, this section isn’t addressing censorship resistance directly; it’s more about enabling the later parts that make ERA’s information available, easily navigable, and useful.

---

# 3. The Access and Navigation Elements of ERA

Now that you have a standardized data format (ideally) and a storage layer (which is verifiable, though not yet fully censorship resistant), you need to consider accessibility. Even with the current setup, you can begin building tools on top of ERA. Since the data is both machine and human readable, platforms similar to what Dune Dashboards has done for crypto transactions or Kaggle for datasets can be envisioned for ERA.

---

# 4. Ensuring Accessibility

Ensuring accessibility, in my view, is synonymous with ensuring censorship resistance. So, how can ERA achieve this? I envision a bidding model for accessibility. Here’s the idea:  
Imagine Luther in America is fighting a case for Snowden. Luther comes across a historical court case that could support privacy litigation. He believes this information will be removed eventually—especially by the new government. So, Luther goes to ERA, generates a checksum of the data along with other verifiable hashes and the content, and uploads it accompanied by a $25 signed transaction using a censorship-resistant stablecoin.  
Various social archivists then see this proposal, which includes a payment for storage and access. They try to store and save the document by providing an access endpoint or website linked to the ERA protocol. Once the data is seeded by enough social archivists, the payout is verified and awarded to the first archivist who made it possible. Others who help seed the data can also anonymously or pseudonymously be supported by the stable coin payment anytime, thereby verifying that the data is indeed being preserved.  
This approach also works in regions that censor websites. For example, if Israel censors Amnesty International data on Gaza, someone or an organization can bid to have that website accessible for two months in Israel, and the ERA protocol will handle the verification and permissionless payment and interested partners can seed the data more if they want and if they don't want or the data doesn't fit the exact "type" of data then its dropped and eventually lost. Social archivists can use any technique to win the bid—whether by uploading on a torrent, storing on IPFS and connecting to their domain, or generating an onion link. There could even be subsidized organizations set up in countries that operate anonymously to take in requests and submit bids for users who are unable to do so themselves. So Luthers bid  once fulfilled can be scraped by AI agents  easily (due to it having a Semantic standard understandable to machines ) of various NGO that can help seed it  further. 
One challenge with any bid model is fee congestion and fee hikes, but I believe this can be mitigated, even if the exact method is not yet clear.
