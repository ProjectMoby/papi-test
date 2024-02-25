# Polkadot Asset Hub Polkadot-API test

- [ ] Type '{ parents: number; interior: XcmV3Junctions; }' is not assignable to type 'number'
- [ ] TransactionError: TxError: invalid - Invalid transaction: BadProof

There is an implementation difference in **ChargeAssetTxPayment** between Westend Asset Hub and Polkadot Asset Hub.

```typescript
//Implementation on Westend Asset Hub
const ChargeAssetTxPaymentAsset: PlainDescriptor<{
  parents: number
  interior: XcmV3Junctions
}> = "cu4kmf2s8kn2k" as PlainDescriptor<{
  parents: number
  interior: XcmV3Junctions
}>

//Implementation on Polkadot Asset Hub
const ChargeAssetTxPaymentAsset: PlainDescriptor<number> =
  "6" as PlainDescriptor<number>
```
