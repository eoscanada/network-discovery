Network Discovery files for EOS.IO Software blockchain launch
-------------------------------------------------------------

Please read the `sample_mainnet.yaml` file diligently.

This repository proposes a protocol for autonomous Block Producers
participation in an EOS.IO Software based blockchain launch.

It is used by the https://github.com/eoscanada/eos-bios program to
boot or help you join a network.

By linking to their `wingmen`, BPs effectively create a graph,
weighted according to their trust in their peers.

The `eos-bios` tool will be able to traverse the graph, fetch all
files references (contracts, snapshots, boot sequences), cache it
locally and use it to execute things on the network.

The main pattern is:
* In your discovery data, you put hashes of the content you vouch
  for. Say you created a `snapshot.csv`, you put the hash in there and
  publish the file.  Everyone, using the tooling can download that
  file, check its hash, and know you vouch for that file.

* If you don't feel like running the machinery for the snapshot, but
  you trust entity XYZ, you can copy their download location and hash,
  and vouch for that hash too. This way, not everyone is forced to run
  the machinery.  It is assumed here that most BPs will want to have
  those who do run the machinery as their wingmen, strengthening
  those who do in the network, but that's all up for grabs.

Any BP capable of publishing a file on the internet can participate.
You are not part of a network until someone already in the network
adds you as one of their _wingmen_. But you can point to a part of
the graph and join the network very easily, no need for special access
to even talk to people, you only need to follow the protocol.
