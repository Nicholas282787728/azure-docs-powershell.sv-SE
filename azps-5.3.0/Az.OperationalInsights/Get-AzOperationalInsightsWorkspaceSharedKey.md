---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527379"
---
# <span data-ttu-id="27711-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="27711-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="27711-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27711-102">SYNOPSIS</span></span>
<span data-ttu-id="27711-103">Hämtar de delade nycklarna för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="27711-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="27711-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27711-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27711-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27711-105">DESCRIPTION</span></span>
<span data-ttu-id="27711-106">Cmdleten **Get-AzOperationalInsightsWorkspaceSharedKey** innehåller de delade nycklarna för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="27711-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="27711-107">Nycklarna används för att koppla operativa insikter till arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="27711-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="27711-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27711-108">EXAMPLES</span></span>

### <span data-ttu-id="27711-109">Exempel 1: Hämta delade nycklar efter arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="27711-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="27711-110">Det här kommandot hämtar de delade nycklarna för arbets ytan med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="27711-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="27711-111">Exempel 2: Hämta delade nycklar genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="27711-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="27711-112">Det här kommandot hämtar arbets ytan med namnet min arbets yta med Get-AzOperationalInsightsWorkspace cmdlet och skickar sedan arbets ytan till cmdleten **Get-AzOperationalInsightsWorkspaceSharedKey** .</span><span class="sxs-lookup"><span data-stu-id="27711-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="27711-113">Kommandot hämtar de delade nycklarna för den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="27711-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="27711-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27711-114">PARAMETERS</span></span>

### <span data-ttu-id="27711-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27711-115">-DefaultProfile</span></span>
<span data-ttu-id="27711-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="27711-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27711-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="27711-117">-Name</span></span>
<span data-ttu-id="27711-118">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="27711-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27711-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27711-119">-ResourceGroupName</span></span>
<span data-ttu-id="27711-120">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="27711-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="27711-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27711-121">CommonParameters</span></span>
<span data-ttu-id="27711-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27711-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27711-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27711-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27711-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27711-124">INPUTS</span></span>

### <span data-ttu-id="27711-125">System. String</span><span class="sxs-lookup"><span data-stu-id="27711-125">System.String</span></span>

## <span data-ttu-id="27711-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27711-126">OUTPUTS</span></span>

### <span data-ttu-id="27711-127">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="27711-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="27711-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27711-128">NOTES</span></span>

## <span data-ttu-id="27711-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27711-129">RELATED LINKS</span></span>

[<span data-ttu-id="27711-130">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="27711-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="27711-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="27711-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


