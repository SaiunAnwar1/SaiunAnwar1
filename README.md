// Connect to the Arweave wallet extension, requesting the SIGNATURE permission
await window.arweaveWallet.connect(["SIGNATURE"]);

// Sign the data using the wallet's signature method
const signature = await window.arweaveWallet.signature(new TextEncoder().encode("Data to sign"), {
  name: 'RSA-PSS', // Use the RSA-PSS algorithm for signing
  saltLength: 0,   // Set the salt length to 0
});

// Log the generated signature to the console
console.log("The signature is", signature);
