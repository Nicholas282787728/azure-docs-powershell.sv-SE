---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: e854d9e77ba72ca297b2b9ca9a8d20f55d6194fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916117"
---
# <span data-ttu-id="4a738-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4a738-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="4a738-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a738-102">SYNOPSIS</span></span>
<span data-ttu-id="4a738-103">Får ett integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="4a738-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="4a738-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a738-104">SYNTAX</span></span>

### <span data-ttu-id="4a738-105">ByIntegrationAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="4a738-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a738-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a738-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a738-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4a738-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a738-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a738-108">DESCRIPTION</span></span>
<span data-ttu-id="4a738-109">Cmdleten **Get-AzIntegrationAccountAssembly** hämtar en sammansättning från ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="4a738-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="4a738-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a738-110">EXAMPLES</span></span>

### <span data-ttu-id="4a738-111">Exempel 1: Hämta en montering efter parametrar</span><span class="sxs-lookup"><span data-stu-id="4a738-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="4a738-112">Skaffa en sammansättning med namnet "sampleAssembly" som finns i integrations kontot, "sampleIntegrationAccount", som finns i resurs gruppen "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="4a738-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="4a738-113">Exempel 2: lista alla sammansättningar i ett integrations konto utifrån parametrar</span><span class="sxs-lookup"><span data-stu-id="4a738-113">Example 2: List all assemblies in an integration account by parameters</span></span>
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

<span data-ttu-id="4a738-114">Hämta alla sammansättningar i integrations kontot "sampleIntegrationAccount" som finns i resurs gruppen "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="4a738-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="4a738-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a738-115">PARAMETERS</span></span>

### <span data-ttu-id="4a738-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a738-116">-DefaultProfile</span></span>
<span data-ttu-id="4a738-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a738-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a738-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a738-118">-Name</span></span>
<span data-ttu-id="4a738-119">Namnet på integrations konto sammansättningen.</span><span class="sxs-lookup"><span data-stu-id="4a738-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="4a738-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="4a738-120">-ParentName</span></span>
<span data-ttu-id="4a738-121">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="4a738-121">The integration account name.</span></span>

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

### <span data-ttu-id="4a738-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4a738-122">-ParentObject</span></span>
<span data-ttu-id="4a738-123">Ett integrations konto objekt.</span><span class="sxs-lookup"><span data-stu-id="4a738-123">An integration account object.</span></span>

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

### <span data-ttu-id="4a738-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4a738-124">-ParentResourceId</span></span>
<span data-ttu-id="4a738-125">ID för integrations konto.</span><span class="sxs-lookup"><span data-stu-id="4a738-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="4a738-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a738-126">-ResourceGroupName</span></span>
<span data-ttu-id="4a738-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4a738-127">The resource group name.</span></span>

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

### <span data-ttu-id="4a738-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a738-128">CommonParameters</span></span>
<span data-ttu-id="4a738-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a738-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a738-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a738-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a738-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a738-131">INPUTS</span></span>

### <span data-ttu-id="4a738-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4a738-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="4a738-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4a738-133">System.String</span></span>

## <span data-ttu-id="4a738-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a738-134">OUTPUTS</span></span>

### <span data-ttu-id="4a738-135">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4a738-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="4a738-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a738-136">NOTES</span></span>

## <span data-ttu-id="4a738-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a738-137">RELATED LINKS</span></span>
