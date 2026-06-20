```
 📥 WEBHOOK INCOMING [20/6/2026, 13.45.28] 
2|dev      | 🔹 [PAYLOAD DATA] RefID: "TRX1781937922516-083821486389" | StatusCode: 0 | Status: "queued"
2|dev      | 🔹 [RAW BODY]: {"refid":"TRX1781937922516-083821486389","kode_reseller":"FS0044","kode_transaksi":"","kode_produk":"XLA14","tujuan":"083821486389","status_code":0,"status":"queued","message":"#107422# XLA14.083821486389 akan diproses @13.45.24. Saldo 397.702 - 42.500 = 355.202R#TRX1781937922516-083821486389","sn":"","harga":43000,"saldo":354702,"tgl_entri":"2026-06-20 13:45:23","tgl_status":"2026-06-20 13:45:28"}
2|dev      | 🔹 [DB SEARCH] Mencari ID Transaksi "TRX1781937922516-083821486389"...
2|dev      | ✅ [DB RESULT] Transaksi Ditemukan! Status saat ini di DB: "pending"
2|dev      | 🎯 [STATUS PENDING] Kode 0 dianggap pending. Menunggu callback selanjutnya.
2|dev      | 
2|dev      |  📥 WEBHOOK INCOMING [20/6/2026, 13.45.28] 
2|dev      | 🔹 [PAYLOAD DATA] RefID: "TRX1781937922516-083821486389" | StatusCode: 1 | Status: "queued"
2|dev      | 🔹 [RAW BODY]: {"refid":"TRX1781937922516-083821486389","kode_reseller":"FS0044","kode_transaksi":"","kode_produk":"","tujuan":"","status_code":1,"status":"queued","message":"#107422# XLA14.083821486389 akan diproses @13.45.24. Saldo 397.702 - 42.500 = 355.202R#TRX1781937922516-083821486389","sn":"","harga":42500,"saldo":-42500,"tgl_entri":"2026-06-20 13:45:28","tgl_status":"2026-06-20 13:45:28"}
2|dev      | 🔹 [DB SEARCH] Mencari ID Transaksi "TRX1781937922516-083821486389"...
2|dev      | ✅ [DB RESULT] Transaksi Ditemukan! Status saat ini di DB: "pending"
2|dev      | 🎯 [STATUS PENDING] Kode 1 dianggap pending. Menunggu callback selanjutnya.
2|dev      | ✅ [DEBUG-GATEWAY]: Respon sukses diterima dari create_trx | Data: {"status":true,"data":{"refid":"TRX1781937922516-083821486389","status":"queued","kode_produk":"XLA14","tujuan":"083821486389","harga":43000,"saldo_awal":397702,"saldo_akhir":354702,"message":"#107422# XLA14.083821486389 akan diproses @13.45.24. Saldo 397.702 - 42.500 = 355.202R#TRX1781937922516-083821486389"}}
2|dev      | 🚀 ~ createOrderSecure ~ provider: MRF
2|dev      | 🚀 ~ createOrderSecure ~ apiResponse: {
2|dev      |   status: true,
2|dev      |   msg: '#107422# XLA14.083821486389 akan diproses @13.45.24. Saldo 397.702 - 42.500 = 355.202R#TRX1781937922516-083821486389'
2|dev      | }
2|dev      | Closing session: SessionEntry {
2|dev      |   _chains: {
2|dev      |     'BXV+IdgoK4q+trN2e+WWTBsH4vVNpFrd7I+ak/96Masy': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     Bc76HhTxYphTcd1cx2a6p1VvpyEC5pLRNQR4dYSAI1Al: { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     BWm8t22tN3ixeeaH5HIi6wA2WTAGMq9fdldM5e9rcJdE: { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BezB4U7+FmPDkGlZ/andiSAxoBsXmwgGfJbbBaYFGaM/': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     BQityLwu6eOKYLWuwZq3cgyg0qwr6stwYIYBXGRtlQcR: { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BYSd/Zku+CfWfXEfh+9AlRdFpcuTfHCH1vPMVUOu6zYI': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BUhm3B+RCV0HpoKgS+7nkWX6MY815DlDL15J1+mffC48': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BXCj/YuQMK2C12LULLL7ceewcLcj32USVz1Kgd6A+Kke': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BQkA7iC6tPG5Wo+JsqYJWFZQO1mM8AN5omMv0PVtVxk0': { chainKey: [Object], chainType: 1, messageKeys: {} }
2|dev      |   },
2|dev      |   registrationId: 537374510,
2|dev      |   currentRatchet: {
2|dev      |     ephemeralKeyPair: {
2|dev      |       pubKey: <Buffer 05 09 00 ee 20 ba b4 f1 b9 5a 8f 89 b2 a6 09 58 56 50 3b 59 8c f0 03 79 a2 63 2f d0 f5 6d 57 19 34>,
2|dev      |       privKey: <Buffer 80 38 97 87 ad ba 90 ac e6 fe a5 f7 6e 31 7b 6d b9 e2 2d 3e 63 47 44 03 9a 14 50 7f fe 36 85 49>
2|dev      |     },
2|dev      |     lastRemoteEphemeralKey: <Buffer 05 70 a3 fd 8b 90 30 ad 82 d7 62 d4 2c b2 fb 71 e7 b0 70 b7 23 df 65 12 57 3d 4a 81 de 80 f8 a9 1e>,
2|dev      |     previousCounter: 2,
2|dev      |     rootKey: <Buffer 37 16 0c ef d8 ae 52 ba aa c3 c2 4b 28 76 2e ae 9b 3a 3e ff e1 76 c4 b6 cd f4 5b 9e d4 24 21 ee>
2|dev      |   },
2|dev      |   indexInfo: {
2|dev      |     baseKey: <Buffer 05 a1 47 37 76 6e 3b 49 e6 04 ba 58 3c 16 26 d3 92 87 80 63 40 fe 0b 48 07 5e d5 db 80 ad 30 49 25>,
2|dev      |     baseKeyType: 1,
2|dev      |     closed: -1,
2|dev      |     used: 1781949542518,
2|dev      |     created: 1781932576421,
2|dev      |     remoteIdentityKey: <Buffer 05 f1 1e 2f 09 b5 79 40 c1 24 aa 5d ae 81 7d 80 2c 77 d4 f6 f8 5c 8c c2 0a 97 19 21 92 b4 2d 7a 19>
2|dev      |   }
2|dev      | }
2|dev      | Closing session: SessionEntry {
2|dev      |   _chains: {
2|dev      |     'BVrWNkd+66fp8BOkcSOwf9bTtBUKYAZoN3O1k+W+xyYw': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BSkKWYU9gFM4M7r1ge3Ys2SLfgfbg+PgYW8DqD7dAG8O': { chainKey: [Object], chainType: 1, messageKeys: {} }
2|dev      |   },
2|dev      |   registrationId: 183628995,
2|dev      |   currentRatchet: {
2|dev      |     ephemeralKeyPair: {
2|dev      |       pubKey: <Buffer 05 29 0a 59 85 3d 80 53 38 33 ba f5 81 ed d8 b3 64 8b 7e 07 db 83 e3 e0 61 6f 03 a8 3e dd 00 6f 0e>,
2|dev      |       privKey: <Buffer 20 2c 74 09 7b a0 c4 fa 5f 23 40 1f bd cd 80 d4 b2 0d ae 7d 16 07 73 f9 13 34 a1 28 30 98 43 77>
2|dev      |     },
2|dev      |     lastRemoteEphemeralKey: <Buffer 05 5a d6 36 47 7e eb a7 e9 f0 13 a4 71 23 b0 7f d6 d3 b4 15 0a 60 06 68 37 73 b5 93 e5 be c7 26 30>,
2|dev      |     previousCounter: 0,
2|dev      |     rootKey: <Buffer 90 21 88 49 7a 64 dd cd 95 e7 b6 6b d9 51 a3 ba e2 c8 b1 85 7b 83 c7 3d a1 0f 25 28 de 69 18 d4>
2|dev      |   },
2|dev      |   indexInfo: {
2|dev      |     baseKey: <Buffer 05 7a 07 a8 52 ae 5d 79 24 a6 3d 02 e4 53 51 eb 13 d8 05 05 6a 74 94 14 3c a8 c1 2e 63 0d 74 98 4b>,
2|dev      |     baseKeyType: 1,
2|dev      |     closed: -1,
2|dev      |     used: 1781915120114,
2|dev      |     created: 1781915105813,
2|dev      |     remoteIdentityKey: <Buffer 05 de 38 d4 5a cd 2c 1a 82 8e 70 b1 99 4b f2 ff 10 ba 16 45 b3 47 cc d0 7d b1 bb 6d 4a a7 4c 99 53>
2|dev      |   }
2|dev      | }
2|dev      | Closing session: SessionEntry {
2|dev      |   _chains: {
2|dev      |     'BVQGY3LxMX8Th5jylNgVUKCU4QBPmZ9I+L2EHGHjBcob': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BUyU/yXJNcK+j3u4vs9OWhF/0CClszY+NjjhFjV453UJ': { chainKey: [Object], chainType: 1, messageKeys: {} }
2|dev      |   },
2|dev      |   registrationId: 1623353637,
2|dev      |   currentRatchet: {
2|dev      |     ephemeralKeyPair: {
2|dev      |       pubKey: <Buffer 05 4c 94 ff 25 c9 35 c2 be 8f 7b b8 be cf 4e 5a 11 7f d0 20 a5 b3 36 3e 36 38 e1 16 35 78 e7 75 09>,
2|dev      |       privKey: <Buffer d0 e4 6a 9b 2b a0 1d 0e d8 b4 a7 80 15 0f 05 d5 6a d2 9d c9 36 5e 30 52 11 9e 31 3a 7a 57 00 61>
2|dev      |     },
2|dev      |     lastRemoteEphemeralKey: <Buffer 05 54 06 63 72 f1 31 7f 13 87 98 f2 94 d8 15 50 a0 94 e1 00 4f 99 9f 48 f8 bd 84 1c 61 e3 05 ca 1b>,
2|dev      |     previousCounter: 0,
2|dev      |     rootKey: <Buffer 9a 35 8e 51 79 91 b2 c3 82 c4 a7 b6 f0 66 25 69 34 f0 6a c8 51 2d 66 e8 ad 6e 98 78 c6 b0 a3 1d>
2|dev      |   },
2|dev      |   indexInfo: {
2|dev      |     baseKey: <Buffer 05 b5 dc 84 f6 f5 f8 c4 f5 1b 11 71 07 37 af 8a 52 61 d3 da 59 7b d0 86 a7 8c 2a f9 92 ae 8d 4f 33>,
2|dev      |     baseKeyType: 1,
2|dev      |     closed: -1,
2|dev      |     used: 1781923294228,
2|dev      |     created: 1781923197296,
2|dev      |     remoteIdentityKey: <Buffer 05 94 02 e1 9b ac 35 62 70 54 8a c4 3b 5b 5a f8 cf c0 bb 2c 07 f4 ff d2 c9 32 20 da 97 01 44 9f 00>
2|dev      |   }
2|dev      | }
2|dev      | Closing session: SessionEntry {
2|dev      |   _chains: {
2|dev      |     'BdviMpNJ/Ic7ueTtLWV3x6ig0aMVEjHOA0VL0QjTw4lI': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     BWIHCwBmlyVPAKLqpzeJvNasteyGJpNBqlCx7XAzgLwV: { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BffvQnJ2nGaJMAdTt0/UI7BExrUSkDeOYQvzLuNQMpEP': { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     'BRFdGSk66xh5G+nVi41c7kr+ZgSgKCgruLK7cjswTGNL': { chainKey: [Object], chainType: 1, messageKeys: {} }
2|dev      |   },
2|dev      |   registrationId: 537374510,
2|dev      |   currentRatchet: {
2|dev      |     ephemeralKeyPair: {
2|dev      |       pubKey: <Buffer 05 11 5d 19 29 3a eb 18 79 1b e9 d5 8b 8d 5c ee 4a fe 66 04 a0 28 28 2b b8 b2 bb 72 3b 30 4c 63 4b>,
2|dev      |       privKey: <Buffer 00 ef 11 7e a7 74 3c 1b 61 11 19 c7 48 61 80 0d 72 dc 7d c6 bb 3b 87 03 dd d1 fb 6e 10 11 49 42>
2|dev      |     },
2|dev      |     lastRemoteEphemeralKey: <Buffer 05 f7 ef 42 72 76 9c 66 89 30 07 53 b7 4f d4 23 b0 44 c6 b5 12 90 37 8e 61 0b f3 2e e3 50 32 91 0f>,
2|dev      |     previousCounter: 0,
2|dev      |     rootKey: <Buffer d2 96 84 b0 ba c9 9d df fd 5d 81 8e 26 8a 95 80 40 38 04 9f 7a 0a 6b 40 08 2d d6 c7 2d 1a 2c 6f>
2|dev      |   },
2|dev      |   indexInfo: {
2|dev      |     baseKey: <Buffer 05 9d 6a 02 cc ae 51 78 0c 3d be bb 55 52 d4 75 44 ab ad 9f 8c 4b 1f 20 c1 0c 39 37 31 cf f8 d5 66>,
2|dev      |     baseKeyType: 1,
2|dev      |     closed: -1,
2|dev      |     used: 1781950656344,
2|dev      |     created: 1781949543416,
2|dev      |     remoteIdentityKey: <Buffer 05 f1 1e 2f 09 b5 79 40 c1 24 aa 5d ae 81 7d 80 2c 77 d4 f6 f8 5c 8c c2 0a 97 19 21 92 b4 2d 7a 19>
2|dev      |   }
2|dev      | }
2|dev      | Closing session: SessionEntry {
2|dev      |   _chains: {
2|dev      |     BQolfzfyOM8a4SDJ9YfOH4yKN7SaFdD9r59pefEvjNdf: { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     BZkI9OOZr2gGcsr9cWdEnki9ecHIC54XkrlGQgycgKom: { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     BRubfsEAQv45d991dHMyVYLfg2lDSkEiINIeqtkdCMVX: { chainKey: [Object], chainType: 2, messageKeys: {} },
2|dev      |     Ba4OXMRnuKgEhce6o4uWINlCIlpmUIUvHATme4RLVMMa: { chainKey: [Object], chainType: 1, messageKeys: {} }
2|dev      |   },
2|dev      |   registrationId: 70134682,
2|dev      |   currentRatchet: {
2|dev      |     ephemeralKeyPair: {
2|dev      |       pubKey: <Buffer 05 ae 0e 5c c4 67 b8 a8 04 85 c7 ba a3 8b 96 20 d9 42 22 5a 66 50 85 2f 1c 04 e6 7b 84 4b 54 c3 1a>,
2|dev      |       privKey: <Buffer a8 11 d0 f5 4d 56 52 4f 74 db 81 67 c1 fc 9c f5 98 ad 8b 63 94 67 03 34 03 23 58 30 a6 fc 59 40>
2|dev      |     },
2|dev      |     lastRemoteEphemeralKey: <Buffer 05 1b 9b 7e c1 00 42 fe 39 77 df 75 74 73 32 55 82 df 83 69 43 4a 41 22 20 d2 1e aa d9 1d 08 c5 57>,
2|dev      |     previousCounter: 0,
2|dev      |     rootKey: <Buffer 9a 91 33 c6 dd 04 79 ec 8b 6c 68 0a 0a 8a ee c6 aa 4d 65 0a 2c 02 b6 96 e7 38 85 24 78 62 93 5c>
2|dev      |   },
2|dev      |   indexInfo: {
2|dev      |     baseKey: <Buffer 05 89 60 23 3c 5f 9e 4d ae 44 8d 39 dd 59 ac 79 c8 e4 a5 a7 41 2f e0 95 05 3f af f4 1f a2 16 92 1a>,
2|dev      |     baseKeyType: 2,
2|dev      |     closed: -1,
2|dev      |     used: 1781950469923,
2|dev      |     created: 1781937182079,
2|dev      |     remoteIdentityKey: <Buffer 05 36 86 23 00 4e 85 2e ee af 38 50 05 59 f3 43 86 b0 00 84 dc 57 9b 7f 98 b4 9d 25 95 8c e8 59 7b>
2|dev      |   }
2|dev      | }
2|dev      | 🚀 ~ createOrderSecure ~ providerName: MRF
2|dev      | 📡 [DEBUG-GATEWAY]: Menembak API create_trx | RefID: TRX1781950687828-087885144703 | Produk: XDA38 | Tujuan: 087885144703
2|dev      | 
2|dev      |  📥 WEBHOOK INCOMING [20/6/2026, 17.18.13] 
2|dev      | 🔹 [PAYLOAD DATA] RefID: "TRX1781950687828-087885144703" | StatusCode: 0 | Status: "queued"
2|dev      | 🔹 [RAW BODY]: {"refid":"TRX1781950687828-087885144703","kode_reseller":"FS0044","kode_transaksi":"","kode_produk":"XDA38","tujuan":"087885144703","status_code":0,"status":"queued","message":"#107490# XDA38.087885144703 akan diproses @17.18.09. Saldo 355.202 - 60.000 = 295.202R#TRX1781950687828-087885144703","sn":"","harga":60000,"saldo":295202,"tgl_entri":"2026-06-20 17:18:08","tgl_status":"2026-06-20 17:18:13"}
2|dev      | 🔹 [DB SEARCH] Mencari ID Transaksi "TRX1781950687828-087885144703"...
2|dev      | ✅ [DB RESULT] Transaksi Ditemukan! Status saat ini di DB: "pending"
2|dev      | 🎯 [STATUS PENDING] Kode 0 dianggap pending. Menunggu callback selanjutnya.
2|dev      | ✅ [DEBUG-GATEWAY]: Respon sukses diterima dari create_trx | Data: {"status":true,"data":{"refid":"TRX1781950687828-087885144703","status":"queued","kode_produk":"XDA38","tujuan":"087885144703","harga":60000,"saldo_awal":355202,"saldo_akhir":295202,"message":"#107490# XDA38.087885144703 akan diproses @17.18.09. Saldo 355.202 - 60.000 = 295.202R#TRX1781950687828-087885144703"}}
2|dev      | 🚀 ~ createOrderSecure ~ provider: MRF
2|dev      | 🚀 ~ createOrderSecure ~ apiResponse: {
2|dev      |   status: true,
2|dev      |   msg: '#107490# XDA38.087885144703 akan diproses @17.18.09. Saldo 355.202 - 60.000 = 295.202R#TRX1781950687828-087885144703'
2|dev      | }
2|dev      | 

```
