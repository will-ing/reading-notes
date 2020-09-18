# SSH

SSH - is a remote administration protocol that allows users to control and modify their remote servers over the Internet

The command consists of 3 distinct parts.

```t
ssh {user}@{host}
```

1. user - represents the account you want to access.
2. host - refers to the computer you want to access.

> advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client.

3 different encryption technologies used by SSH

1. `Symmetrical encryption `- A secret key is used for both encryption and decryption of a message by both the client and the host
2. `Asymmetrical encryption` - Uses two separate keys for encryption and decryption.
   1. is not used to encrypt the entire SSH session
   2. only used during the key exchange algorithm of symmetric encryption
3. `Hashing` - Generate a unique value of a fixed length for each input that shows no clear trend which can exploited. This makes them practically impossible to reverse.
   1. `HMACs`, or Hash-based Message Authentication Codes.

> Both the client and the server agree on a very large prime number, which of course does not have any factor in common. This prime number value is also known as the seed value.

username and password - These credentials securely pass through the symmetrically encrypted tunnel, so there is no chance of them being captured by a third party.

[Main Page](https://will-ing.github.io/reading-notes)