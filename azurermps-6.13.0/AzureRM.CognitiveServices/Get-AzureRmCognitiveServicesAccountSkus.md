---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580835"
---
# <span data-ttu-id="90447-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="90447-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="90447-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90447-102">SYNOPSIS</span></span>
<span data-ttu-id="90447-103">Hämtar tillgängliga SKU: er för ett konto.</span><span class="sxs-lookup"><span data-stu-id="90447-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90447-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90447-104">SYNTAX</span></span>

### <span data-ttu-id="90447-105">GetSkusWithAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="90447-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90447-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="90447-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90447-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90447-107">DESCRIPTION</span></span>
<span data-ttu-id="90447-108">Cmdleten **Get-AzureRmCognitiveServicesAccountSkus** hämtar tillgängliga SKU: er för ett kognitivt Services-konto.</span><span class="sxs-lookup"><span data-stu-id="90447-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="90447-109">SKU är en nivå plan för ett konto.</span><span class="sxs-lookup"><span data-stu-id="90447-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="90447-110">Det definierar priset, samtals gränsen och kostnaden för kontot.</span><span class="sxs-lookup"><span data-stu-id="90447-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="90447-111">F0 SKU är en kostnads fri nivå.</span><span class="sxs-lookup"><span data-stu-id="90447-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="90447-112">Betalda nivåer är S0, S1, S2 och så vidare.</span><span class="sxs-lookup"><span data-stu-id="90447-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="90447-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90447-113">EXAMPLES</span></span>

### <span data-ttu-id="90447-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="90447-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="90447-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90447-115">PARAMETERS</span></span>

### <span data-ttu-id="90447-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90447-116">-DefaultProfile</span></span>
<span data-ttu-id="90447-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="90447-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90447-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="90447-118">-Location</span></span>
<span data-ttu-id="90447-119">Konto plats för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="90447-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90447-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="90447-120">-Name</span></span>
<span data-ttu-id="90447-121">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="90447-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90447-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90447-122">-ResourceGroupName</span></span>
<span data-ttu-id="90447-123">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="90447-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90447-124">– Skriv</span><span class="sxs-lookup"><span data-stu-id="90447-124">-Type</span></span>
<span data-ttu-id="90447-125">Konto typen för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="90447-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90447-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90447-126">CommonParameters</span></span>
<span data-ttu-id="90447-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90447-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90447-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90447-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90447-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90447-129">INPUTS</span></span>

### <span data-ttu-id="90447-130">System. String</span><span class="sxs-lookup"><span data-stu-id="90447-130">System.String</span></span>

## <span data-ttu-id="90447-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90447-131">OUTPUTS</span></span>

### <span data-ttu-id="90447-132">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="90447-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="90447-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90447-133">NOTES</span></span>

## <span data-ttu-id="90447-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90447-134">RELATED LINKS</span></span>
