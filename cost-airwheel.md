# Custos do Projeto Airwheel - Brasil e Paraguai

## Visão Geral
Este documento detalha os custos estimados para desenvolver e implantar duas plataformas de e-commerce para o Projeto Airwheel, uma para o Brasil e outra para o Paraguai, usando os planos Pro de Vercel (frontend), MongoDB Atlas M10 (banco de dados), Render (backend) e Cloudinary Free (gerenciamento de arquivos), com integração de servidores de arquivos para acesso moderado. O email profissional usa o plano Microsoft 365 Business Basic. Os custos são divididos em cronograma padrão (13 semanas por país, paralelo) e acelerado (2 semanas por país, paralelo).

## Premissas
- **Taxas Horárias** (baseadas no mercado da América Latina, 2025):
  - Gerente de Projeto (PM): $50/hora
  - Designer UI/UX: $40/hora
  - Desenvolvedor Backend: $45/hora
  - Desenvolvedor Frontend: $45/hora
  - Engenheiro DevOps: $50/hora
  - Engenheiro de QA: $35/hora
- **Taxa de Câmbio**: R$ 5,50/USD
- **Infraestrutura**:
  - Vercel: Plano Pro ($40/mês por país, 2 desenvolvedores)
  - MongoDB Atlas: Cluster M10 ($57/mês por país) + Data Federation ($4,50/mês para 50GB de transferência)
  - Render: Instância Pro ($45/mês por país) + Disco ($5/mês para 20GB)
  - Cloudinary: Plano Free ($0/mês, 25GB de armazenamento, 20GB de largura de banda)
  - Domínios: .com.br (R$ 40/ano), .com.py ($30/ano)
  - WHOIS Privacy: $0 (Brasil, não aplicável), $15/ano (Paraguai)
  - Email: Microsoft 365 Business Basic ($72/ano por país, 1 usuário)
  - APIs de Envio: Correios ($9/mês, Brasil), AEX ($10/mês, Paraguai)
- **Exclusões**: Taxas de gateways de pagamento (e.g., Mercado Pago: ~4,99% + R$ 0,50/transação; Bancard: ~5%/transação) variam com o volume de vendas e não são incluídas nos custos fixos.

## Custos do Cronograma Acelerado (2 semanas, paralelo)
### Brasil
- **Mão de Obra**:
  - PM: 40 horas × $50 = $2.000
  - Designer UI/UX: 25 horas × $40 = $1.000
  - Desenvolvedor Backend: 65 horas × $45 = $2.925
  - Desenvolvedor Frontend: 60 horas × $45 = $2.700
  - Engenheiro DevOps: 20 horas × $50 = $1.000
  - Engenheiro de QA: 15 horas × $35 = $525
  - **Subtotal**: $10.150
- **Infraestrutura** (1 mês):
  - Domínio (.com.br): $7,27/ano (R$ 40)
  - WHOIS Privacy: $0 (não aplicável)
  - Vercel (Pro): $40/mês × 1 = $40
  - MongoDB Atlas (M10 + Data Federation): ($57 + $4,50) × 1 = $61,50
  - Render (Pro + Disco): ($45 + $5) × 1 = $50
  - Cloudinary (Free): $0/mês × 1 = $0
  - Email (Microsoft 365 Business Basic): $72/ano (~$6 para 1 mês)
  - API de Envio (Correios): $9/mês × 1 = $9
  - **Subtotal**: $172,77
- **Total Brasil**: $10.322,77

### Paraguai
- **Mão de Obra**: $10.150 (mesmo que Brasil)
- **Infraestrutura** (1 mês):
  - Domínio (.com.py): $30/ano
  - WHOIS Privacy: $15/ano
  - Vercel (Pro): $40/mês × 1 = $40
  - MongoDB Atlas (M10 + Data Federation): ($57 + $4,50) × 1 = $61,50
  - Render (Pro + Disco): ($45 + $5) × 1 = $50
  - Cloudinary (Free): $0/mês × 1 = $0
  - Email (Microsoft 365 Business Basic): $72/ano (~$6 para 1 mês)
  - API de Envio (AEX): $10/mês × 1 = $10
  - **Subtotal**: $211,50
- **Total Paraguai**: $10.361,50

### Total (Ambos)
- $10.322,77 (Brasil) + $10.361,50 (Paraguai) = **$20.684,27**

## Notas
- **Vercel**: O plano Pro ($20/mês por desenvolvedor, 2 desenvolvedores por país) suporta tráfego moderado (1TB de largura de banda) e integração com Cloudinary via API. Monitore custos de largura de banda extra ($0,15/GB,).
- **MongoDB Atlas**: O cluster M10 ($57/mês) é adequado para e-commerce com tráfego moderado, com Data Federation ($4,50/mês para 50GB) para integração com Cloudinary. Clusters M0 são inadequados devido a limitações ().
- **Render**: A instância Pro ($45/mês) com disco ($5/mês para 20GB) suporta APIs de tráfego moderado e integração com Vercel/Cloudinary. Instâncias maiores ($85/mês) podem ser necessárias para picos de tráfego.
- **Cloudinary**: O plano Free ($0/mês) suporta 25GB de armazenamento e 20GB de largura de banda, suficiente para e-commerce inicial com otimizações (compressão de imagens). Monitore uso para evitar custos extras ($0,10/GB,).
- **Email**: Microsoft 365 Business Basic ($72/ano por usuário) oferece email profissional (50GB) e integração com domínios personalizados ().
- **Domínios**: .com.br baseado em Registro.br (R$ 40/ano,); .com.py estimado ($30/ano) devido a dados limitados.
- **Taxas de Transação**: Excluídas dos cálculos fixos, pois dependem do volume de vendas. Recomenda-se revisar Mercado Pago e Bancard para estimativas precisas.
- **Riscos**: Picos de tráfego podem aumentar custos no Vercel ($0,15/GB extra,), Render ($0,25/GB extra para discos), ou Cloudinary ($0,10/GB extra). Usar Vercel Spend Management para limites de gasto ().

## Recomendações
- **Cronograma Acelerado**: Adequado para entrada rápida no mercado ($20.684,27), mas pode exigir manutenção adicional.
- **Otimização de Custos**:
  - Use caching (e.g., ISR no Vercel) para reduzir custos de largura de banda ().
  - Monitore operações de leitura/escrita no MongoDB Atlas para evitar custos excessivos ().
  - Configure discos no Render com tamanho mínimo viável para economizar.
  - Otimize imagens no Cloudinary (compressão, formatos eficientes como WebP) para permanecer no plano gratuito ().
  - Verifique a disponibilidade dos domínios (.com.br, .com.py) antes do orçamento.
- **Próximos Passos**:
  - Registrar domínios via Registro.br (Brasil) e um registrador confiável (Paraguai).
  - Configurar contas no Vercel, MongoDB Atlas, Render e Cloudinary com integração via GitHub para deploy automático.
  - Configurar email no Microsoft 365 com domínios personalizados ().
  - Testar APIs de pagamento, envio e Cloudinary em ambientes sandbox para evitar custos inesperados.
  - Implementar monitoramento (e.g., Vercel Analytics, Cloudinary Insights) para otimizar uso de recursos ().
