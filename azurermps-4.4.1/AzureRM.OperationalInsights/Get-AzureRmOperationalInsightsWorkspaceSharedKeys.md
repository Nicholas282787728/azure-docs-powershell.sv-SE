---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 884d2a4168a4ce9efd27a6ae46387dae048f9ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577584"
---
# <span data-ttu-id="bd18c-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="bd18c-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="bd18c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd18c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd18c-103">Hämtar de delade nycklarna för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="bd18c-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd18c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd18c-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd18c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd18c-105">DESCRIPTION</span></span>
<span data-ttu-id="bd18c-106">Cmdleten **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** innehåller de delade nycklarna för en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="bd18c-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="bd18c-107">Nycklarna används för att koppla operativa insikter till arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="bd18c-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="bd18c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd18c-108">EXAMPLES</span></span>

### <span data-ttu-id="bd18c-109">Exempel 1: Hämta delade nycklar efter arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="bd18c-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="bd18c-110">Det här kommandot hämtar de delade nycklarna för arbets ytan med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bd18c-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="bd18c-111">Exempel 2: Hämta delade nycklar genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="bd18c-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="bd18c-112">Det här kommandot hämtar arbets ytan med namnet min arbets yta med Get-AzureRmOperationalInsightsWorkspace cmdlet och skickar sedan arbets ytan till cmdleten **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** .</span><span class="sxs-lookup"><span data-stu-id="bd18c-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="bd18c-113">Kommandot hämtar de delade nycklarna för den arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="bd18c-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="bd18c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd18c-114">PARAMETERS</span></span>

### <span data-ttu-id="bd18c-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd18c-115">-Name</span></span>
<span data-ttu-id="bd18c-116">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="bd18c-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="bd18c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd18c-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd18c-118">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="bd18c-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="bd18c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd18c-119">-DefaultProfile</span></span>
<span data-ttu-id="bd18c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd18c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd18c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd18c-121">CommonParameters</span></span>
<span data-ttu-id="bd18c-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd18c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd18c-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd18c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd18c-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd18c-124">INPUTS</span></span>

## <span data-ttu-id="bd18c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd18c-125">OUTPUTS</span></span>

### <span data-ttu-id="bd18c-126">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="bd18c-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="bd18c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd18c-127">NOTES</span></span>

## <span data-ttu-id="bd18c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd18c-128">RELATED LINKS</span></span>

[<span data-ttu-id="bd18c-129">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="bd18c-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="bd18c-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="bd18c-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

