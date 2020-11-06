---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 230c47e67610cdeea629097f26c73cb2774c5384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579635"
---
# <span data-ttu-id="06e32-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="06e32-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="06e32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="06e32-102">SYNOPSIS</span></span>
<span data-ttu-id="06e32-103">Hämtar API-nycklarna för ett konto.</span><span class="sxs-lookup"><span data-stu-id="06e32-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06e32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="06e32-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06e32-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="06e32-105">DESCRIPTION</span></span>
<span data-ttu-id="06e32-106">Cmdleten **Get-AzureRmCognitiveServicesAccountKey** hämtar API-nycklarna för ett etablerat konto för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="06e32-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="06e32-107">Ett konto för kognitiva tjänster har två API-nycklar: KEY1 och Key2.</span><span class="sxs-lookup"><span data-stu-id="06e32-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="06e32-108">Nycklarna aktiverar interaktion med konto slut punkten för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="06e32-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="06e32-109">Använd New-AzureRmCognitiveServicesAccountKey för att återskapa en nyckeln.</span><span class="sxs-lookup"><span data-stu-id="06e32-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="06e32-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="06e32-110">EXAMPLES</span></span>

## <span data-ttu-id="06e32-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="06e32-111">PARAMETERS</span></span>

### <span data-ttu-id="06e32-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e32-112">-DefaultProfile</span></span>
<span data-ttu-id="06e32-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="06e32-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e32-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="06e32-114">-Name</span></span>
<span data-ttu-id="06e32-115">Anger namnet på kontot.</span><span class="sxs-lookup"><span data-stu-id="06e32-115">Specifies the name of the account.</span></span>
<span data-ttu-id="06e32-116">Denna cmdlet hämtar nycklarna för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="06e32-116">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e32-117">-ResourceGroupName</span></span>
<span data-ttu-id="06e32-118">Anger namnet på resurs gruppen som kontot är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="06e32-118">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e32-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e32-119">CommonParameters</span></span>
<span data-ttu-id="06e32-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e32-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e32-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e32-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e32-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="06e32-122">INPUTS</span></span>

### <span data-ttu-id="06e32-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="06e32-123">None</span></span>
<span data-ttu-id="06e32-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="06e32-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06e32-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="06e32-125">OUTPUTS</span></span>

### <span data-ttu-id="06e32-126">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="06e32-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="06e32-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="06e32-127">NOTES</span></span>

## <span data-ttu-id="06e32-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="06e32-128">RELATED LINKS</span></span>

[<span data-ttu-id="06e32-129">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="06e32-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


