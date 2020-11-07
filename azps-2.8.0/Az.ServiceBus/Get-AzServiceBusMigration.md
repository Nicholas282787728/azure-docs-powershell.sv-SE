---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 1e782c381ec10d03f269fc0a2d0871f064e4ddef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919217"
---
# <span data-ttu-id="ac889-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="ac889-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="ac889-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac889-102">SYNOPSIS</span></span>
<span data-ttu-id="ac889-103">Hämtar MigrationConfiguration för namn området</span><span class="sxs-lookup"><span data-stu-id="ac889-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="ac889-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac889-104">SYNTAX</span></span>

### <span data-ttu-id="ac889-105">MigrationConfigurationPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ac889-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac889-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ac889-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ac889-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac889-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac889-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac889-108">DESCRIPTION</span></span>
<span data-ttu-id="ac889-109">Konfigurationen **för migrering** för namn området hämtas</span><span class="sxs-lookup"><span data-stu-id="ac889-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="ac889-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac889-110">EXAMPLES</span></span>

### <span data-ttu-id="ac889-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ac889-111">Example 1</span></span>
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

<span data-ttu-id="ac889-112">Hämtar egenskaperna för migreringsguiden för TestingNamespaceStandardMigration</span><span class="sxs-lookup"><span data-stu-id="ac889-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="ac889-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac889-113">PARAMETERS</span></span>

### <span data-ttu-id="ac889-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac889-114">-DefaultProfile</span></span>
<span data-ttu-id="ac889-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac889-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac889-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac889-116">-InputObject</span></span>
<span data-ttu-id="ac889-117">Namespace-objekt</span><span class="sxs-lookup"><span data-stu-id="ac889-117">Namespace Object</span></span>

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

### <span data-ttu-id="ac889-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac889-118">-Name</span></span>
<span data-ttu-id="ac889-119">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="ac889-119">Namespace Name</span></span>

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

### <span data-ttu-id="ac889-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac889-120">-ResourceGroupName</span></span>
<span data-ttu-id="ac889-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ac889-121">Resource Group Name</span></span>

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

### <span data-ttu-id="ac889-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac889-122">-ResourceId</span></span>
<span data-ttu-id="ac889-123">Namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="ac889-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="ac889-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac889-124">CommonParameters</span></span>
<span data-ttu-id="ac889-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac889-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac889-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac889-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac889-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac889-127">INPUTS</span></span>

### <span data-ttu-id="ac889-128">Microsoft. Azure. commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ac889-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="ac889-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ac889-129">System.String</span></span>

## <span data-ttu-id="ac889-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac889-130">OUTPUTS</span></span>

### <span data-ttu-id="ac889-131">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ac889-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="ac889-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac889-132">NOTES</span></span>

## <span data-ttu-id="ac889-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac889-133">RELATED LINKS</span></span>
