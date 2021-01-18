---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525209"
---
# <span data-ttu-id="ce419-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="ce419-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="ce419-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ce419-102">SYNOPSIS</span></span>
<span data-ttu-id="ce419-103">Få åtkomst till RAW-åtkomsttoken.</span><span class="sxs-lookup"><span data-stu-id="ce419-103">Get raw access token.</span></span> <span data-ttu-id="ce419-104">När du använder-ResourceUrl kontrollerar du att värdet stämmer överens med den aktuella Azure-miljön.</span><span class="sxs-lookup"><span data-stu-id="ce419-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="ce419-105">Du kan referera till värdet i `(Get-AzContext).Environment` .</span><span class="sxs-lookup"><span data-stu-id="ce419-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="ce419-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ce419-106">SYNTAX</span></span>

### <span data-ttu-id="ce419-107">KnownResourceTypeName (standard)</span><span class="sxs-lookup"><span data-stu-id="ce419-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce419-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="ce419-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce419-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ce419-109">DESCRIPTION</span></span>
<span data-ttu-id="ce419-110">Hämta åtkomsttoken</span><span class="sxs-lookup"><span data-stu-id="ce419-110">Get access token</span></span>

## <span data-ttu-id="ce419-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ce419-111">EXAMPLES</span></span>

### <span data-ttu-id="ce419-112">Exempel 1 Hämta token för RAW-åtkomst för ARM slut punkt</span><span class="sxs-lookup"><span data-stu-id="ce419-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="ce419-113">Hämta åtkomst-token för slut punkten för det aktuella kontot</span><span class="sxs-lookup"><span data-stu-id="ce419-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="ce419-114">Exempel 2 Hämta åtkomsttoken för Access-graf för AAD</span><span class="sxs-lookup"><span data-stu-id="ce419-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="ce419-115">Hämta Access-token för AAD-slutpunktsmappare för aktuellt konto</span><span class="sxs-lookup"><span data-stu-id="ce419-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="ce419-116">Exempel 3 Hämta åtkomsttoken för Access-graf för AAD</span><span class="sxs-lookup"><span data-stu-id="ce419-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="ce419-117">Hämta Access-token för AAD-slutpunktsmappare för aktuellt konto</span><span class="sxs-lookup"><span data-stu-id="ce419-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="ce419-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ce419-118">PARAMETERS</span></span>

### <span data-ttu-id="ce419-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce419-119">-DefaultProfile</span></span>
<span data-ttu-id="ce419-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ce419-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce419-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="ce419-121">-ResourceTypeName</span></span>
<span data-ttu-id="ce419-122">Valfritt namn på reresurs-typ, tillåtna värden: AadGraph, AnalysisServices, arm, attestering, batch, DataLake,, OperationalInsights, ResourceManager, Synapse.</span><span class="sxs-lookup"><span data-stu-id="ce419-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="ce419-123">Standardvärdet är arm om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="ce419-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce419-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="ce419-124">-ResourceUrl</span></span>
<span data-ttu-id="ce419-125">Resurs-URL för att begära token, till exempel " http://graph.windows.net/ ".</span><span class="sxs-lookup"><span data-stu-id="ce419-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce419-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="ce419-126">-TenantId</span></span>
<span data-ttu-id="ce419-127">Valfritt klient-ID. Använd klient-ID för standard kontext om det inte anges.</span><span class="sxs-lookup"><span data-stu-id="ce419-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce419-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce419-128">CommonParameters</span></span>
<span data-ttu-id="ce419-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce419-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce419-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce419-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce419-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ce419-131">INPUTS</span></span>

### <span data-ttu-id="ce419-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="ce419-132">None</span></span>

## <span data-ttu-id="ce419-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ce419-133">OUTPUTS</span></span>

### <span data-ttu-id="ce419-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ce419-134">System.String</span></span>

## <span data-ttu-id="ce419-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ce419-135">NOTES</span></span>

## <span data-ttu-id="ce419-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ce419-136">RELATED LINKS</span></span>
