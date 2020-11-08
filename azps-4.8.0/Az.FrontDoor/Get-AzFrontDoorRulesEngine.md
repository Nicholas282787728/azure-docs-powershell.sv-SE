---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/get-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Get-AzFrontDoorRulesEngine.md
ms.openlocfilehash: c0742344db01e40a01a0aeee3b61b93b92cc3f07
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262684"
---
# <span data-ttu-id="eef05-101">Get-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="eef05-101">Get-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="eef05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eef05-102">SYNOPSIS</span></span>
<span data-ttu-id="eef05-103">Skaffa regler för regel motor.</span><span class="sxs-lookup"><span data-stu-id="eef05-103">Get Rules Engine configurations.</span></span>

## <span data-ttu-id="eef05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eef05-104">SYNTAX</span></span>

```
Get-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef05-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eef05-105">DESCRIPTION</span></span>
<span data-ttu-id="eef05-106">Cmdleten **Get-AzFrontDoorRulesEngine** hämtar en specifik regel motor konfiguration eller får alla regel motor konfigurationer som är kopplade till en front dörr.</span><span class="sxs-lookup"><span data-stu-id="eef05-106">The **Get-AzFrontDoorRulesEngine** cmdlet gets a specific rules engine configuration or gets all rules engine configurations associated with a Front Door.</span></span> 

## <span data-ttu-id="eef05-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eef05-107">EXAMPLES</span></span>

### <span data-ttu-id="eef05-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eef05-108">Example 1</span></span>
```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name rulesengine3

Name         RulesEngineRules
----         ----------------
rulesEngine3 {rules1}
```

<span data-ttu-id="eef05-109">Skaffa specifika regel motor konfiguration.</span><span class="sxs-lookup"><span data-stu-id="eef05-109">Get specific rules engine configuration.</span></span>

### <span data-ttu-id="eef05-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="eef05-110">Example 2</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName

Name         RulesEngineRules
----         ----------------
rulesEngine1 {Rule1}
rulesEngine2 {Rule1}
rulesEngine3 {rules1}
```

<span data-ttu-id="eef05-111">Få alla inställningar för regel motor i en front dörr.</span><span class="sxs-lookup"><span data-stu-id="eef05-111">Get all rules engine configurations in a front door.</span></span>

### <span data-ttu-id="eef05-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="eef05-112">Example 3</span></span>

```powershell
PS C:\> Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistent
Get-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistent' in Front Door 'frontDoorName' is not found.
At line:1 char:1
+ Get-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontD ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Get-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.GetFrontDoorRulesEngine
```

<span data-ttu-id="eef05-113">Förväntade utdata när du skaffar en regel motor som inte finns.</span><span class="sxs-lookup"><span data-stu-id="eef05-113">Expected output when getting a nonexistent rules engine.</span></span> 

## <span data-ttu-id="eef05-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eef05-114">PARAMETERS</span></span>

### <span data-ttu-id="eef05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef05-115">-DefaultProfile</span></span>
<span data-ttu-id="eef05-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eef05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eef05-117">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="eef05-117">-FrontDoorName</span></span>
<span data-ttu-id="eef05-118">Namn på främre dörren.</span><span class="sxs-lookup"><span data-stu-id="eef05-118">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eef05-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="eef05-119">-Name</span></span>
<span data-ttu-id="eef05-120">Namn på regel motor.</span><span class="sxs-lookup"><span data-stu-id="eef05-120">Rules engine name.</span></span>

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

### <span data-ttu-id="eef05-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef05-121">-ResourceGroupName</span></span>
<span data-ttu-id="eef05-122">Namnet på den resurs grupp som ska skapas i.</span><span class="sxs-lookup"><span data-stu-id="eef05-122">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eef05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef05-123">CommonParameters</span></span>
<span data-ttu-id="eef05-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef05-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eef05-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef05-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eef05-126">INPUTS</span></span>

### <span data-ttu-id="eef05-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="eef05-127">None</span></span>

## <span data-ttu-id="eef05-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eef05-128">OUTPUTS</span></span>

### <span data-ttu-id="eef05-129">Microsoft. Azure. commands. FrontDoor. Models. PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="eef05-129">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

## <span data-ttu-id="eef05-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eef05-130">NOTES</span></span>

## <span data-ttu-id="eef05-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eef05-131">RELATED LINKS</span></span>
