// connect to the extension
await window.arweaveWallet.connect(
  // request permissions to read the active address
  ["ACCESS_ADDRESS"],
  // provide some extra info for our app
  {
    name: "Super Cool App",
    logo: "https://arweave.net/jAvd7Z1CBd8gVF2D6ESj7SMCCUYxDX_z3vpp5aHdaYk",
  },
  // custom gateway
  {
    host: "g8way.io",
    port: 443,
    protocol: "https",
  }
);
