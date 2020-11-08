---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273402"
---
# <span data-ttu-id="2abcd-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2abcd-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="2abcd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2abcd-102">SYNOPSIS</span></span>
<span data-ttu-id="2abcd-103">Hämtar en batch-konfiguration för integrerings konton.</span><span class="sxs-lookup"><span data-stu-id="2abcd-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="2abcd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2abcd-104">SYNTAX</span></span>

### <span data-ttu-id="2abcd-105">ByIntegrationAccount (standard)</span><span class="sxs-lookup"><span data-stu-id="2abcd-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2abcd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2abcd-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2abcd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2abcd-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2abcd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2abcd-108">DESCRIPTION</span></span>
<span data-ttu-id="2abcd-109">Cmdleten **Get-AzIntegrationAccountBatchConfiguration** hämtar en grupp konfiguration från ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="2abcd-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="2abcd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2abcd-110">EXAMPLES</span></span>

### <span data-ttu-id="2abcd-111">Exempel 1: Hämta en grupp konfiguration efter parametrar</span><span class="sxs-lookup"><span data-stu-id="2abcd-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="2abcd-112">Hämta en grupp konfiguration med namnet "sampleBatchConfig" i integrations kontot "sampleIntegrationAccount" som finns i resurs gruppen "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="2abcd-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="2abcd-113">Exempel 2: lista alla kommandofiler i ett integrations konto efter parametrar</span><span class="sxs-lookup"><span data-stu-id="2abcd-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="2abcd-114">Hämta alla kommandofiler i integrerings kontot "sampleIntegrationAccount" som finns i resurs gruppen "sampleResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="2abcd-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="2abcd-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2abcd-115">PARAMETERS</span></span>

### <span data-ttu-id="2abcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abcd-116">-DefaultProfile</span></span>
<span data-ttu-id="2abcd-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2abcd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2abcd-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2abcd-118">-Name</span></span>
<span data-ttu-id="2abcd-119">Namnet på batch-konfigurationsfilen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="2abcd-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abcd-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="2abcd-120">-ParentName</span></span>
<span data-ttu-id="2abcd-121">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="2abcd-121">The integration account name.</span></span>

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

### <span data-ttu-id="2abcd-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2abcd-122">-ParentObject</span></span>
<span data-ttu-id="2abcd-123">Ett integrations konto objekt.</span><span class="sxs-lookup"><span data-stu-id="2abcd-123">An integration account object.</span></span>

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

### <span data-ttu-id="2abcd-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2abcd-124">-ParentResourceId</span></span>
<span data-ttu-id="2abcd-125">ID för integrations konto.</span><span class="sxs-lookup"><span data-stu-id="2abcd-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="2abcd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2abcd-126">-ResourceGroupName</span></span>
<span data-ttu-id="2abcd-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2abcd-127">The resource group name.</span></span>

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

### <span data-ttu-id="2abcd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abcd-128">CommonParameters</span></span>
<span data-ttu-id="2abcd-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2abcd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abcd-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2abcd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abcd-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2abcd-131">INPUTS</span></span>

### <span data-ttu-id="2abcd-132">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="2abcd-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="2abcd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2abcd-133">System.String</span></span>

## <span data-ttu-id="2abcd-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2abcd-134">OUTPUTS</span></span>

### <span data-ttu-id="2abcd-135">Microsoft. Azure. commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2abcd-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="2abcd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2abcd-136">NOTES</span></span>

## <span data-ttu-id="2abcd-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2abcd-137">RELATED LINKS</span></span>
