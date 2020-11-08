---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099230"
---
# <span data-ttu-id="21012-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="21012-101">New-AzureProfile</span></span>

## <span data-ttu-id="21012-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21012-102">SYNOPSIS</span></span>

## <span data-ttu-id="21012-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21012-103">SYNTAX</span></span>

### <span data-ttu-id="21012-104">Upplåsningscertifikat</span><span class="sxs-lookup"><span data-stu-id="21012-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="21012-105">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21012-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="21012-106">Korrelation</span><span class="sxs-lookup"><span data-stu-id="21012-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="21012-107">Administratörsautentisering</span><span class="sxs-lookup"><span data-stu-id="21012-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="21012-108">Tomt</span><span class="sxs-lookup"><span data-stu-id="21012-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="21012-109">Fil</span><span class="sxs-lookup"><span data-stu-id="21012-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="21012-110">PropertyBag</span><span class="sxs-lookup"><span data-stu-id="21012-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="21012-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21012-111">DESCRIPTION</span></span>

## <span data-ttu-id="21012-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21012-112">EXAMPLES</span></span>

### <span data-ttu-id="21012-113">9.1</span><span class="sxs-lookup"><span data-stu-id="21012-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="21012-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21012-114">PARAMETERS</span></span>

### <span data-ttu-id="21012-115">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="21012-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-116">-AccountId</span><span class="sxs-lookup"><span data-stu-id="21012-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-117">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="21012-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21012-118">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="21012-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-119">-Miljö</span><span class="sxs-lookup"><span data-stu-id="21012-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-120">-Path</span><span class="sxs-lookup"><span data-stu-id="21012-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-121">-Egenskaper</span><span class="sxs-lookup"><span data-stu-id="21012-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-122">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21012-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="21012-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="21012-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-125">-Klient organisationen</span><span class="sxs-lookup"><span data-stu-id="21012-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21012-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21012-126">CommonParameters</span></span>
<span data-ttu-id="21012-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21012-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21012-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21012-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21012-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21012-129">INPUTS</span></span>

## <span data-ttu-id="21012-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21012-130">OUTPUTS</span></span>

## <span data-ttu-id="21012-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21012-131">NOTES</span></span>

## <span data-ttu-id="21012-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21012-132">RELATED LINKS</span></span>

