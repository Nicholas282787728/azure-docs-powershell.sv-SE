---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326088"
---
# <span data-ttu-id="3fe59-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="3fe59-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="3fe59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fe59-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe59-103">Hämta Azure Advisor-konfigurationerna för den angivna prenumerationen eller resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3fe59-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="3fe59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fe59-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fe59-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fe59-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe59-106">Konfigurationer kopplade till en prenumeration har två typer:</span><span class="sxs-lookup"><span data-stu-id="3fe59-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="3fe59-107">Prenumerations nivå konfiguration: det kan bara finnas en konfiguration av den här typen för en prenumeration.</span><span class="sxs-lookup"><span data-stu-id="3fe59-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="3fe59-108">LowCpuThreshold och exkludera är den enda egenskapen för den här typen av konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fe59-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="3fe59-109">ResourceGroup nivå konfiguration: det kan bara finnas en konfiguration för varje ResourceGroup i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3fe59-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="3fe59-110">Exkludera är den enda egenskapen för den här typen av konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3fe59-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="3fe59-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fe59-111">EXAMPLES</span></span>

### <span data-ttu-id="3fe59-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3fe59-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="3fe59-113">Hämtar en lista med Azure Advisor-konfiguration (er).</span><span class="sxs-lookup"><span data-stu-id="3fe59-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="3fe59-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fe59-114">PARAMETERS</span></span>

### <span data-ttu-id="3fe59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe59-115">-DefaultProfile</span></span>
<span data-ttu-id="3fe59-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fe59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fe59-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe59-117">-ResourceGroupName</span></span>
<span data-ttu-id="3fe59-118">Konfigurationens resurs grupp namn</span><span class="sxs-lookup"><span data-stu-id="3fe59-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fe59-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe59-119">CommonParameters</span></span>
<span data-ttu-id="3fe59-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe59-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3fe59-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fe59-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe59-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fe59-122">INPUTS</span></span>

### <span data-ttu-id="3fe59-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="3fe59-123">None</span></span>

## <span data-ttu-id="3fe59-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fe59-124">OUTPUTS</span></span>

### <span data-ttu-id="3fe59-125">Microsoft. Azure. commands. rådgivare. cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="3fe59-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="3fe59-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fe59-126">NOTES</span></span>

## <span data-ttu-id="3fe59-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fe59-127">RELATED LINKS</span></span>