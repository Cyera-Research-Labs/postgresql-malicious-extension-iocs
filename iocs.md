# Indicators of Compromise

Last verified: 2026-09-27

---

## gc_manager Campaign (PostgreSQL Extensions)

### C2 Domains

| Domain | Registrar | First Seen | Status |
|---|---|---|---|
| `asq.d6shiiwz.pw` | REG.RU (Moscow) | 2019-10 | Active |
| `asd.s7610rir.pw` | REG.RU (Moscow) | 2021-01 | Active |
| `us1.somepools555.pw` | Namecheap | 2023-04 | Active |
| `asq.r77vh0.pw` | REG.RU (Moscow) | 2018-06 | Inactive |
| `d1.pool4883.pw` | REG.RU (Moscow) | 2025-07 | Active |

### C2 IPs

```
194.48.248.39
209.99.186.219
```

### Windows gc_manager.dll (16 samples)

```
0637c029845110b90146a894a860cf26c7bf0b6eaa95f49b4341501f53b35acc
1568c7d6b09687b06393278d2f991a1b1efeef1c2c22b42b149758d04fd99af9
2b3ea1144f566a00251f56f779f64bbc1ae97876809940f49a37535df159295e
3480d4d59f6a5746b8fd952239055931fe03fa7143d3a36ae5c524857ae8d522
41804f1467275f436d3a5303ecb3bea1ef1f8130e54248aa9888ff3f580af2dd
450ad26a041e51950956b109a22990ddc46786de46919ddeb2224f9dbbcfe846
8730dd940ec7242c4f72dcd9698652063c88f8bdc23b88c18e7e41a45f00e439
9a53b5d6fcb8a0ebe6704e9375b100e910cc12e80a8bdebecb6e57f598e5ea8a
c46c1c9dfc3b728fb01dda53721eeab3631fb6b84efeed72d54ec8f3fce937db
e06b7118082d5ff0638c62992a2a372ae81fbfe42bf969a966dd6bcde18ca5a4
e8e1ad75b7d767d71b446670d72e92d44c3a0d95bf1d334fe26941f040140c99
f038250f31c06b84ba2e58561b51f22b5c30482c84077c55880a557a756e4d82
f86cdfebc776c063aa1077b7cc72d10d63f5129b7a88a91b6dec95350c2ade84
01b3b47e5df62cafc91ec32c34777d38fc71929cadfd7ce6fe5c4d38eeba7033
1c49f99450d4f77c98c973cbe16d60cdbd2b87575530d55fd54d06873ce19bb7
bbf1caaa3c5926ea742871b8210204c3913dba89a842fc7f146cb54e3f00ec2f
```

### Linux gcmanager-1.so (4 samples)

```
fb0e952804714034640a45ca09fff87b74b0ec7ae2a11ed8bd5b4096895526f1
715348a40250549100cbbeb2a8d68ffa323e671b55fc46e8df24c7016b11e10a
97109072c04bd4a4806bb7172a2a3128dfe10bf83fccea31217d5a9ad0b1b503
d3f6f1de753bceef33dd4515c50a436b2c5a687cbb795122921fddabcb3391f4
```

### Embedded Payloads

```
d3bb71a7554dbeeb248d35db4d03514ed84e4023b21ef7e21616cb0c6fb5a053  # Windows Stage 2 downloader
52422f2470fcccfbc40e55bb5c273ad3db947e92ec0474f83ddf423a2c50cf5b  # Linux Stage 2 downloader
```

### c64.exe (XMRigCC Miner - downloaded by Windows Stage 2)

```
47e777c4541044dd439bf065478bfadc5b6d7049f70a3114ca8386acb02d0b6a
```

### xmrig (XMRigCC Miner - downloaded by Linux Stage 2)

```
287bd345c4cd16737ab999d8f9fd08ebb9411d09d06c35aa4869d65db31367e1
```

### Mining Pools

```
eu.minerpool.pw:443
rig.zxcvb.pw:443
rig.myrms.pw:443
rs.fym5gserobhh.pw:443
back123.brasilia.me:443
185.10.68.220:443
65.87.7.196:443
2.59.220.122:443
```

---

## patch.exe Campaign (Azorult Stealer) - Same Actor, Different Delivery

### C2 Infrastructure

```
lubrpenal.xyz/ynvs2/index.php
interstart.xyz/hab3v13/index.php
testarea.hostigger.com
195.123.234.33
141.98.117.69
```

### patch.exe (6 samples)

```
02178169ec7cd5abd69d5537614b3c1c9b85bc00902cebd048c2aba8c9d770ea
a22e1bf0009fa6cdbd4fe8dcf974feb583f237b1dfdbdf7b137ac9b0c99488ac
93166bc5f43d374777823bb4eefc72c2b9d960d5f6bf8fd1f76ebe06627f7eed
2984122ebc7466fc38153921570a1bf64439e79a5849003d652c1d2beabd4610
1dfd0162fc8d9b52c8ae9634219b8e59100fafad1c98e64335dcce62c8c254cb
ef299f9f764df01505a86404828e9fa54df31ba1e1cabcd737db6d6ae0b490e5
```

### Azorult Stealer (dropped by patch.exe)

```
2c54175c5b7755e11726fa7bd1b2c9e7f681bded3af3a77c7916bb15acac505a
```

---

**Note:** two hashes above are not present in VirusTotal, because they were never submitted:

- `d3bb71a7554dbeeb248d35db4d03514ed84e4023b21ef7e21616cb0c6fb5a053` — the Windows Stage 2
  exists only after in-memory decryption, so it is never written to disk.
- `47e777c4541044dd439bf065478bfadc5b6d7049f70a3114ca8386acb02d0b6a` — retrieved directly
  from the C2 on 2026-07-26.
