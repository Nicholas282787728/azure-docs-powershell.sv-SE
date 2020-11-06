---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41d217579175de3c1de6f36b6850dfd391ca04b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578336"
---
# <span data-ttu-id="e3743-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3743-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="e3743-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3743-102">SYNOPSIS</span></span>
<span data-ttu-id="e3743-103">Hämtar ett konto.</span><span class="sxs-lookup"><span data-stu-id="e3743-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3743-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3743-104">SYNTAX</span></span>

### <span data-ttu-id="e3743-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3743-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3743-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3743-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3743-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3743-107">DESCRIPTION</span></span>
<span data-ttu-id="e3743-108">Cmdleten **Get-AzureRmCognitiveServicesAccount** hämtar de etablerade kontona för kognitiva tjänster i resurs gruppen som anges av parametern *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="e3743-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="e3743-109">Om du inte anger parametern *ResoureGroupName* hämtar denna cmdlet alla kognitiva tjänst konton för den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="e3743-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="e3743-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3743-110">EXAMPLES</span></span>

## <span data-ttu-id="e3743-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3743-111">PARAMETERS</span></span>

### <span data-ttu-id="e3743-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3743-112">-DefaultProfile</span></span>
<span data-ttu-id="e3743-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e3743-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3743-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3743-114">-Name</span></span>
<span data-ttu-id="e3743-115">Anger namnet på det konto som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="e3743-115">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3743-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3743-116">-ResourceGroupName</span></span>
<span data-ttu-id="e3743-117">Anger namnet på resurs gruppen som är kopplat till det här kontot.</span><span class="sxs-lookup"><span data-stu-id="e3743-117">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3743-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3743-118">CommonParameters</span></span>
<span data-ttu-id="e3743-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3743-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3743-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3743-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3743-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3743-121">INPUTS</span></span>

### <span data-ttu-id="e3743-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="e3743-122">None</span></span>
<span data-ttu-id="e3743-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e3743-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e3743-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3743-124">OUTPUTS</span></span>

### <span data-ttu-id="e3743-125">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3743-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="e3743-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3743-126">NOTES</span></span>

## <span data-ttu-id="e3743-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3743-127">RELATED LINKS</span></span>

[<span data-ttu-id="e3743-128">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3743-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="e3743-129">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3743-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="e3743-130">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="e3743-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


