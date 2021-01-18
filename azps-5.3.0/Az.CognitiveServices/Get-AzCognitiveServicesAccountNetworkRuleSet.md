---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524591"
---
# <span data-ttu-id="d0b4d-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0b4d-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d0b4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0b4d-102">SYNOPSIS</span></span>
<span data-ttu-id="d0b4d-103">Hämta egenskapen NetworkRule för ett konto för kognitiva tjänster</span><span class="sxs-lookup"><span data-stu-id="d0b4d-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="d0b4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0b4d-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0b4d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0b4d-105">DESCRIPTION</span></span>
<span data-ttu-id="d0b4d-106">Cmdleten **Get-AzCognitiveServicesAccountNetworkRuleSet** hämtar egenskapen NetworkRule för ett kognitivt Services-konto</span><span class="sxs-lookup"><span data-stu-id="d0b4d-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="d0b4d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0b4d-107">EXAMPLES</span></span>

### <span data-ttu-id="d0b4d-108">Exempel 1: get NetworkRule-egenskapen för ett angivet kognitivt-konto</span><span class="sxs-lookup"><span data-stu-id="d0b4d-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="d0b4d-109">Det här kommandot får egenskapen NetworkRule för ett angivet kognitivt-konto</span><span class="sxs-lookup"><span data-stu-id="d0b4d-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="d0b4d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0b4d-110">PARAMETERS</span></span>

### <span data-ttu-id="d0b4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0b4d-111">-DefaultProfile</span></span>
<span data-ttu-id="d0b4d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d0b4d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0b4d-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0b4d-113">-Name</span></span>
<span data-ttu-id="d0b4d-114">Konto namn för kognitiva tjänster.</span><span class="sxs-lookup"><span data-stu-id="d0b4d-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b4d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0b4d-115">-ResourceGroupName</span></span>
<span data-ttu-id="d0b4d-116">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d0b4d-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0b4d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0b4d-117">CommonParameters</span></span>
<span data-ttu-id="d0b4d-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0b4d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0b4d-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0b4d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0b4d-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0b4d-120">INPUTS</span></span>

### <span data-ttu-id="d0b4d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d0b4d-121">System.String</span></span>

## <span data-ttu-id="d0b4d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0b4d-122">OUTPUTS</span></span>

### <span data-ttu-id="d0b4d-123">Microsoft. Azure. commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0b4d-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d0b4d-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0b4d-124">NOTES</span></span>

## <span data-ttu-id="d0b4d-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0b4d-125">RELATED LINKS</span></span>
