---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100856"
---
# <span data-ttu-id="ee6c6-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ee6c6-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="ee6c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ee6c6-103">Hämtar MigrationConfiguration för namn området</span><span class="sxs-lookup"><span data-stu-id="ee6c6-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="ee6c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee6c6-104">SYNTAX</span></span>

### <span data-ttu-id="ee6c6-105">MigrationConfigurationPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ee6c6-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee6c6-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ee6c6-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee6c6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee6c6-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee6c6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee6c6-108">DESCRIPTION</span></span>
<span data-ttu-id="ee6c6-109">Konfigurationen **för migrering** för namn området hämtas</span><span class="sxs-lookup"><span data-stu-id="ee6c6-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="ee6c6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee6c6-110">EXAMPLES</span></span>

### <span data-ttu-id="ee6c6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee6c6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="ee6c6-112">Hämtar egenskaperna för migreringsguiden för TestingNamespaceStandardMigration</span><span class="sxs-lookup"><span data-stu-id="ee6c6-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="ee6c6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee6c6-113">PARAMETERS</span></span>

### <span data-ttu-id="ee6c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee6c6-114">-DefaultProfile</span></span>
<span data-ttu-id="ee6c6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee6c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee6c6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee6c6-116">-InputObject</span></span>
<span data-ttu-id="ee6c6-117">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="ee6c6-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee6c6-118">-Name</span></span>
<span data-ttu-id="ee6c6-119">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="ee6c6-119">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee6c6-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee6c6-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ee6c6-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee6c6-122">-ResourceId</span></span>
<span data-ttu-id="ee6c6-123">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="ee6c6-123">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee6c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee6c6-124">CommonParameters</span></span>
<span data-ttu-id="ee6c6-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee6c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee6c6-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee6c6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee6c6-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee6c6-127">INPUTS</span></span>

### <span data-ttu-id="ee6c6-128">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ee6c6-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="ee6c6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ee6c6-129">System.String</span></span>

## <span data-ttu-id="ee6c6-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee6c6-130">OUTPUTS</span></span>

### <span data-ttu-id="ee6c6-131">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ee6c6-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="ee6c6-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee6c6-132">NOTES</span></span>

## <span data-ttu-id="ee6c6-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee6c6-133">RELATED LINKS</span></span>
