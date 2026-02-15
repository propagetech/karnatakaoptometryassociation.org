You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "contact.html",
    "context": {
      "title": "Karnataka Optometry Association | Contact",
      "first_heading": "Contact Us"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/5e3a198b9f557dce8bcf744d800929a9.css",
    "context": {
      "path": "css/5e3a198b9f557dce8bcf744d800929a9.css"
    }
  },
  {
    "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css",
    "context": {
      "path": "css/5ecf9a22a9fea377b8fd4e5d4a7d1a70.css"
    }
  },
  {
    "path": "css/6d95c421cfdc25743ca3bee482775041.css",
    "context": {
      "path": "css/6d95c421cfdc25743ca3bee482775041.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "downloads.html",
    "context": {
      "title": "Karnataka Optometry Association | Downloads",
      "first_heading": "Downloads"
    }
  },
  {
    "path": "events.html",
    "context": {
      "title": "Karnataka Optometry Association | Events",
      "first_heading": "Events"
    }
  },
  {
    "path": "imgs/09f52c2207c628b00ce6fdb1767014bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0a6c04e0eee3cedc0edf8b0eb0dd3429.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e8fd01f14be7651dd46546aa449a8ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10c227dd79e5b854b912b079c754bd3a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b091670e8182d61c9f3dcd7e29e4a1a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1d9ed6355b41230aa9d69ad89ef483c8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1fb47bb5597e703499392c0adc49c875.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/238b4d0a82e429ecc1807d934ce38eb7.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0060",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/239ee5de15ff4ab4ed4a67c133668381.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2452a7d76c85c5fcec8ba9207a6b5af4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/25b22d219026c2176baeedfcf131e539.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2abc564bb2952578c7bf4b0571cec4d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2bd4a108f2d039a09ae595fc51a19d92.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20250226at195820",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/323ad2d19132b6fcf1dad27aa3f71480.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/331b599ce1a6bda395543ccc98908b14.webp",
    "context": {
      "refs": [
        {
          "alt": "Who is an Optometrist?",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/34f73614eb463de9332a2863e011800b.webp",
    "context": {
      "refs": [
        {
          "alt": "DIWAKARRAO",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/372e104704de744d8260c8e7d72ea0d4.webp",
    "context": {
      "refs": [
        {
          "alt": "RajeshGTreasurer",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/37f0a2b28f26711a9e339d78ded36f57.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b929fa2537bbfe694d3e886df4075a9.webp",
    "context": {
      "refs": [
        {
          "alt": "SUBRAMANYASHETTYHS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3bcd8f843c6198439bf086c1892bd4e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3f3235f3bccf5f4fcbaa034ce7a288eb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3fb3824e213d2477b02848fa8b9d672f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/426ecec4fd792653c0b82c864622a047.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/449008fa532e477085291d0927fef311.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4495a404187bfe463332dcea5a2b5bda.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/48b1ebbfbd35e08f889f09f6bacee48d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e7e504c34233a969ab20d12d091a117.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/51c95ace0f09e450b807fdfa736a87a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55377f2fc83236e9f14ebfd16492ec28.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/570b47fdaedd78b43d5cb7d81de18be6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/61f85fd2f3f5f8921a1db5e99b50b03b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65bfb5b8564c47e928be74d68e52ca24.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/677e87d41ae3b2b0fafb38f08dbd5b43.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/68c0c4f50578a0c565e9630590b6232e.webp",
    "context": {
      "refs": [
        {
          "alt": "DEEPTHI",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a8eece176b3e9863838e12aad77fc4d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6db58db87e3ee4d0738a84559e806f71.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7063cabcdcfb6014a33e88c291f3c9fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/752cc4ae5b6de754f916b74bfdd5d805.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0078",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7660e71674375bca8bb31ca8e5de80ad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76a2c71b25ccebb0c5eb4445b7995916.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78f09e96ad4cd95ebb4a8d16292d1469.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7e63352c4d7b79da7eaf5e265d0320dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81d710435798a0cea22ec4d85d8f7249.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/835f9c7976eaae62b576ea511df61d57.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8777e6fabbc9a6a97ac2db21374bb832.webp",
    "context": {
      "refs": [
        {
          "alt": "VIJAYREDDY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/89e887f7a5b56c002c81b222ea739359.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0074",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b0d0fe0e6ee59293d855a4d9e29b538.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d6fd10a9079d7dac4955b06fb1f9a28.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8f017db69f6c108440cf042e340be6fa.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0066",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/93c3282d1fd99520442991e8f9ba470c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/96909ae875470ffe9fc611dbca8f4277.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0071",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/98aaf43978ec0a8c6c3a47148516f0b5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c5cccff7491135f7f3e50ab0d66c895.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20230405201131",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c9d7ae1a4306f68de539f1151c4a0c6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d9accebbb23a2387eb60e97da604708.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Mission",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ec31f26555f3893eab79956869d6b24.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0063",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a09c77a5fcc41631ac0536c44f55bec6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a38ab5ae586c6e7703d56b9ad193c421.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a432606bb9d395d9ed61be2017a3ff92.webp",
    "context": {
      "refs": [
        {
          "alt": "DEEPAGKSECRETORY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a4be6cfe8ecbaa2995e2521f22a74ac5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a556763ded15b0b8828b3d7bac169172.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad0f8611ec1ef19d3ed5d79601e1794e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae011111fb8b66e794020e862adba03b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b04fe98c427f873e9ebf8494a000a584.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0eba1afb273cbf3b0be47ac207c28c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bafe41ccdda55155c38229152832b719.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4dc7af874c838f0227eb8c660c14715.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cc3708fe00246b461b5d9391b0e59152.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ddf45675bcb4c7da806db85440ec0fc2.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Vision",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de1a4103f761e037746bba3d84aa367d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e7beea0f18ae02c4e61a64d0206c241b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e931d67752990bf7168b760485e91367.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0068",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ea167bc61c09724398f0f78b0ed22de7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb7902be28fd5c84dff90f3f77724bfe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec4106ec4609046cd394109cb72f4a85.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0073",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ecb0219afbe6a91cbab3efecc4880d23.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2ead99a89cebaaaf09b3a1910df4b17.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f41f5c5450f57b0996f92888579a2d17.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4cd4b0d403747eb6785e266328f44a6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f72ec0f2a04c5a48397bfd7944863780.webp",
    "context": {
      "refs": [
        {
          "alt": "ppml",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f80945ec360e64b5b18400d32168f7db.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fbc8cf4532a7773bd6fcded4f47d0d84.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc51178f42e129d3c4e41bccffd1828c.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG20250224WA0076",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fce38e0032bd0f4a7067375accb5ebd9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fee263212166d882d4d58062fa74de72.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Karnataka Optometry Association | Home",
      "first_heading": "Welcome toKarnataka Optometry Association"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "members.html",
    "context": {
      "title": "Karnataka Optometry Association | Members",
      "first_heading": "Members"
    }
  },
  {
    "path": "office-bearers.html",
    "context": {
      "title": "Karnataka Optometry Association | Office Bearers",
      "first_heading": "Office Bearers"
    }
  },
  {
    "path": "registration.html",
    "context": {
      "title": "Karnataka Optometry Association | Registration",
      "first_heading": "Membership Registration"
    }
  },
  {
    "path": "terms-and-conditions.html",
    "context": {
      "title": "Karnataka Optometry Association | Terms & Conditions",
      "first_heading": "Terms & Conditions"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.