---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 891f7fcd50281f5dab9b8d4eaf9f1bd842fbc85e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574623"
---
# <span data-ttu-id="72437-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="72437-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="72437-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72437-102">SYNOPSIS</span></span>
<span data-ttu-id="72437-103">Hämtar ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="72437-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72437-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72437-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72437-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72437-105">DESCRIPTION</span></span>
<span data-ttu-id="72437-106">Cmdleten **Get-AzureRmLogicApp** får ett logiskt program.</span><span class="sxs-lookup"><span data-stu-id="72437-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="72437-107">Denna cmdlet returnerar ett **arbets flödes** objekt.</span><span class="sxs-lookup"><span data-stu-id="72437-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="72437-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="72437-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="72437-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="72437-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="72437-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="72437-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="72437-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="72437-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="72437-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72437-112">EXAMPLES</span></span>

### <span data-ttu-id="72437-113">Exempel 1: Hämta ett logik program från en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="72437-113">Example 1: Get a logic app from a resource group</span></span>
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

<span data-ttu-id="72437-114">Det här kommandot får ett logiskt program från resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="72437-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="72437-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72437-115">PARAMETERS</span></span>

### <span data-ttu-id="72437-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="72437-116">-Name</span></span>
<span data-ttu-id="72437-117">Anger namnet på det logik program som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="72437-117">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="72437-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72437-118">-ResourceGroupName</span></span>
<span data-ttu-id="72437-119">Anger namnet på en resurs grupp där denna cmdlet får ett logiskt program.</span><span class="sxs-lookup"><span data-stu-id="72437-119">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="72437-120">-Version</span><span class="sxs-lookup"><span data-stu-id="72437-120">-Version</span></span>
<span data-ttu-id="72437-121">Anger versionen för en logik-app.</span><span class="sxs-lookup"><span data-stu-id="72437-121">Specifies the version of a logic app.</span></span>

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

### <span data-ttu-id="72437-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72437-122">-DefaultProfile</span></span>
<span data-ttu-id="72437-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72437-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72437-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72437-124">CommonParameters</span></span>
<span data-ttu-id="72437-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72437-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72437-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72437-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72437-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72437-127">INPUTS</span></span>

## <span data-ttu-id="72437-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72437-128">OUTPUTS</span></span>

### <span data-ttu-id="72437-129">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="72437-129">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="72437-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72437-130">NOTES</span></span>

## <span data-ttu-id="72437-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72437-131">RELATED LINKS</span></span>

[<span data-ttu-id="72437-132">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="72437-132">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="72437-133">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="72437-133">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="72437-134">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="72437-134">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="72437-135">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="72437-135">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


