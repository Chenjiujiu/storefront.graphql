<div style="text-align: center">

# scheme.graphql App
`@Copyright 2023 By micas`

`shopify storefrontAPI 的 apollographql scheme 参数`

![](https://img.shields.io/static/v1?label=storefront&message=2023-07&color=brightgreen)
</div>

******

> storefrontAPI版本`2023-07`
使用方法    

[Apollo客户端官方文档](https://www.apollographql.com/docs/react/development-testing/static-typing/)  

[The perfect GraphQL Developer Experience](https://the-guild.dev/graphql/codegen/docs/getting-started#the-perfect-graphql-developer-experience)
>`yarn add -D typescript @graphql-codegen/cli @graphql-codegen/client-preset`  

## 创建codegen.ts
```typescript
import { CodegenConfig } from '@graphql-codegen/cli';

const config: CodegenConfig = {
  schema: '<本项目 index.graphql路径>',
  documents: ['src/**/*.tsx'],
  generates: {
    './src/__generated__/': {
      preset: 'client',
      plugins: [],
      presetConfig: {
        gqlTagName: 'gql',
      }
    }
  },
  ignoreNoDocuments: true,
};

export default config;

```


