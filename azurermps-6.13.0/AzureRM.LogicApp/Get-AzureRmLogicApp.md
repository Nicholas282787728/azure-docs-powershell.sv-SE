---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 740ef9b21a2e2caa839880ff2c5e9dadc042351a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584196"
---
# <span data-ttu-id="ca968-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ca968-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="ca968-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ca968-102">SYNOPSIS</span></span>
<span data-ttu-id="ca968-103">Hämtar ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ca968-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca968-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ca968-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca968-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ca968-105">DESCRIPTION</span></span>
<span data-ttu-id="ca968-106">Cmdleten **Get-AzureRmLogicApp** får ett logiskt program.</span><span class="sxs-lookup"><span data-stu-id="ca968-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="ca968-107">Denna cmdlet returnerar ett **arbets flödes** objekt.</span><span class="sxs-lookup"><span data-stu-id="ca968-107">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="ca968-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="ca968-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ca968-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="ca968-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ca968-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="ca968-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ca968-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="ca968-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ca968-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ca968-112">EXAMPLES</span></span>

### <span data-ttu-id="ca968-113">Exempel 1: Hämta ett logik program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="ca968-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="ca968-114">Det här kommandot får ett logiskt program från resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ca968-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ca968-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ca968-115">PARAMETERS</span></span>

### <span data-ttu-id="ca968-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca968-116">-DefaultProfile</span></span>
<span data-ttu-id="ca968-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ca968-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca968-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ca968-118">-Name</span></span>
<span data-ttu-id="ca968-119">Anger namnet på det logik program som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="ca968-119">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca968-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca968-120">-ResourceGroupName</span></span>
<span data-ttu-id="ca968-121">Anger namnet på en resurs grupp där denna cmdlet får ett logiskt program.</span><span class="sxs-lookup"><span data-stu-id="ca968-121">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca968-122">-Version</span><span class="sxs-lookup"><span data-stu-id="ca968-122">-Version</span></span>
<span data-ttu-id="ca968-123">Anger versionen för en logik-app.</span><span class="sxs-lookup"><span data-stu-id="ca968-123">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="ca968-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca968-124">CommonParameters</span></span>
<span data-ttu-id="ca968-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca968-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca968-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca968-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca968-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ca968-127">INPUTS</span></span>

### <span data-ttu-id="ca968-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ca968-128">System.String</span></span>

## <span data-ttu-id="ca968-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ca968-129">OUTPUTS</span></span>

### <span data-ttu-id="ca968-130">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="ca968-130">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="ca968-131">Microsoft. Azure. Management. Logic. Models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="ca968-131">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="ca968-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ca968-132">NOTES</span></span>

## <span data-ttu-id="ca968-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ca968-133">RELATED LINKS</span></span>

[<span data-ttu-id="ca968-134">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ca968-134">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="ca968-135">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ca968-135">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="ca968-136">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ca968-136">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="ca968-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ca968-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

