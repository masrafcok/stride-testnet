# Selamlar, stride için gerekli görevleri yapıyoruz, çok basit.


# Likidite - Staking görevi: 

* Cüzdan adınızı ekleyin.

```
strided tx stakeibc liquid-stake 1000 uatom --from CÜZDAN ADINIZ --chain-id STRIDE-1 --gas 500000 -y
```

# Redeem görevi:

* Cosmos: cüzdanı kısmına KEPLR'da yazan GAIA ağını ekleyın.
* From: kısmı cüzdan adınız

```
strided tx stakeibc redeem-stake 500 GAIA cosmos1vm6wnmvxugqj8k6s6d2cktgctc550qaq50kyye  --chain-id STRIDE-1 --from rues --gas 500000 -y
```

# Bu görevin Komutunda düzenlemeniz gereken tek kısım adres, adresi explorer üzerinde ki cüzdan adresiniz yapın. (Account: https://stride.explorers.guru/)
```
strided q records list-user-redemption-record --output json | jq --arg WALLET_ADDRESS "stride1d6v2gd0hzzg8hp7jzkfsp8uyqd5hh5tsnvjxuv" '.UserRedemptionRecord | map(select(.sender == $WALLET_ADDRESS))'
```

# IBC görevi:

* Sei adresi yazan yer, kendi adresiniz olacak
* From cüzdan adınız olcak.
* Altta channeleri vericem istediğiniz channela gönderin.
* Stafi: channel-15
* Sei: channel-22 
* Altta ki 

```
strided tx ibc-transfer -y transfer transfer channel-22 sei1654kj35pszp4t49wcglwcg0cwlxg5vvw8rv32t 10000ibc/27394FB092D2ECCD56123C74F36E4C1F926001CEADA9CA97EA622B25F41E5EB2  --chain-id STRIDE-1 --from rues
```

# FORM DOLDURUN

https://docs.google.com/forms/d/e/1FAIpQLSfdDrh5-WIsY6LlwVElFfoWR8dZdlE70vHujIMBiD-4USvpsg/viewform

# İŞLEMLER BU KADAR, GÜNCELLEME GELİRSE EKLERİM
