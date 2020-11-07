---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: ca0871dae696425c7f19ac1924aa0b725d0dac6c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926546"
---
# <span data-ttu-id="d263d-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d263d-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="d263d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d263d-102">SYNOPSIS</span></span>
<span data-ttu-id="d263d-103">Hämtar ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d263d-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="d263d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d263d-104">SYNTAX</span></span>

### <span data-ttu-id="d263d-105">ListWorkflows (standard)</span><span class="sxs-lookup"><span data-stu-id="d263d-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d263d-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="d263d-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d263d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d263d-107">DESCRIPTION</span></span>
<span data-ttu-id="d263d-108">Cmdleten **Get-AzLogicApp** får ett logiskt program.</span><span class="sxs-lookup"><span data-stu-id="d263d-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="d263d-109">Denna cmdlet returnerar ett **arbets flödes** objekt.</span><span class="sxs-lookup"><span data-stu-id="d263d-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="d263d-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="d263d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d263d-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="d263d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d263d-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="d263d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d263d-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="d263d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d263d-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d263d-114">EXAMPLES</span></span>

### <span data-ttu-id="d263d-115">Exempel 1: Hämta ett logik program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="d263d-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="d263d-116">Det här kommandot får ett logiskt program från resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d263d-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d263d-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d263d-117">PARAMETERS</span></span>

### <span data-ttu-id="d263d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d263d-118">-DefaultProfile</span></span>
<span data-ttu-id="d263d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d263d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d263d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d263d-120">-Name</span></span>
<span data-ttu-id="d263d-121">Anger namnet på det logik program som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d263d-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d263d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d263d-122">-ResourceGroupName</span></span>
<span data-ttu-id="d263d-123">Anger namnet på en resurs grupp där denna cmdlet får ett logiskt program.</span><span class="sxs-lookup"><span data-stu-id="d263d-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d263d-124">-Version</span><span class="sxs-lookup"><span data-stu-id="d263d-124">-Version</span></span>
<span data-ttu-id="d263d-125">Anger versionen för en logik-app.</span><span class="sxs-lookup"><span data-stu-id="d263d-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d263d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d263d-126">CommonParameters</span></span>
<span data-ttu-id="d263d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d263d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d263d-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d263d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d263d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d263d-129">INPUTS</span></span>

### <span data-ttu-id="d263d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d263d-130">System.String</span></span>

## <span data-ttu-id="d263d-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d263d-131">OUTPUTS</span></span>

### <span data-ttu-id="d263d-132">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="d263d-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="d263d-133">Microsoft. Azure. Management. Logic. Models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="d263d-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="d263d-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d263d-134">NOTES</span></span>

## <span data-ttu-id="d263d-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d263d-135">RELATED LINKS</span></span>

[<span data-ttu-id="d263d-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d263d-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="d263d-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d263d-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="d263d-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d263d-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="d263d-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d263d-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


