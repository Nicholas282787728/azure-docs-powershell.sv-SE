---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259567"
---
# <span data-ttu-id="8295a-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8295a-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="8295a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8295a-102">SYNOPSIS</span></span>
<span data-ttu-id="8295a-103">Får ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="8295a-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="8295a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8295a-104">SYNTAX</span></span>

### <span data-ttu-id="8295a-105">ByIntegrationAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="8295a-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8295a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8295a-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8295a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8295a-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8295a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8295a-108">DESCRIPTION</span></span>
<span data-ttu-id="8295a-109">Cmdleten **Get-AzIntegrationAccountAssembly** hämtar en sammansättning från ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="8295a-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="8295a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8295a-110">EXAMPLES</span></span>

### <span data-ttu-id="8295a-111">Exempel 1: Hämta en montering efter parametrar</span><span class="sxs-lookup"><span data-stu-id="8295a-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="8295a-112">Skaffa en sammansättning med namnet "sampleAssembly" som finns i integrations kontot, "sampleIntegrationAccount", som finns i resurs gruppen "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="8295a-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="8295a-113">Exempel 2: lista alla sammansättningar i ett integrations konto utifrån parametrar</span><span class="sxs-lookup"><span data-stu-id="8295a-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="8295a-114">Hämta alla sammansättningar i integrations kontot "sampleIntegrationAccount" som finns i resurs gruppen "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="8295a-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="8295a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8295a-115">PARAMETERS</span></span>

### <span data-ttu-id="8295a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8295a-116">-DefaultProfile</span></span>
<span data-ttu-id="8295a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8295a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8295a-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="8295a-118">-Name</span></span>
<span data-ttu-id="8295a-119">Namnet på integrations konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="8295a-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8295a-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="8295a-120">-ParentName</span></span>
<span data-ttu-id="8295a-121">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="8295a-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8295a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8295a-122">-ParentObject</span></span>
<span data-ttu-id="8295a-123">Ett integrations konto objekt.</span><span class="sxs-lookup"><span data-stu-id="8295a-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8295a-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8295a-124">-ParentResourceId</span></span>
<span data-ttu-id="8295a-125">ID för integrations konto.</span><span class="sxs-lookup"><span data-stu-id="8295a-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8295a-126">-ResourceGroupName</span></span>
<span data-ttu-id="8295a-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8295a-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8295a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8295a-128">CommonParameters</span></span>
<span data-ttu-id="8295a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8295a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8295a-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8295a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8295a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8295a-131">INPUTS</span></span>

### <span data-ttu-id="8295a-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8295a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="8295a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8295a-133">System.String</span></span>

## <span data-ttu-id="8295a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8295a-134">OUTPUTS</span></span>

### <span data-ttu-id="8295a-135">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="8295a-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="8295a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8295a-136">NOTES</span></span>

## <span data-ttu-id="8295a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8295a-137">RELATED LINKS</span></span>