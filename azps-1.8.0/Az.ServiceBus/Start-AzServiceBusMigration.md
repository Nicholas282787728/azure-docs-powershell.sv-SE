---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 66d8f15c58d1b4b92f19e23f5940ed7c8ba45d3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746860"
---
# <span data-ttu-id="dc6d1-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="dc6d1-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="dc6d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="dc6d1-103">Skapar en ny migrering och börjar migrera enheter från standard till premie namn områden</span><span class="sxs-lookup"><span data-stu-id="dc6d1-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="dc6d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc6d1-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc6d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc6d1-105">DESCRIPTION</span></span>
<span data-ttu-id="dc6d1-106">Cmdleten **Start-AzServiceBusMigration** skapar en ny migrering och börjar migrera enheter från standard till premie namn områden</span><span class="sxs-lookup"><span data-stu-id="dc6d1-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="dc6d1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc6d1-107">EXAMPLES</span></span>

### <span data-ttu-id="dc6d1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc6d1-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="dc6d1-109">Skapar en ny migrerings konfiguration för ' TestingNamespaceStandardMirgation ' till ' TestingNamespacePremiumMirgation '-namn områden</span><span class="sxs-lookup"><span data-stu-id="dc6d1-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="dc6d1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc6d1-110">PARAMETERS</span></span>

### <span data-ttu-id="dc6d1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc6d1-111">-AsJob</span></span>
<span data-ttu-id="dc6d1-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dc6d1-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc6d1-113">-DefaultProfile</span></span>
<span data-ttu-id="dc6d1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc6d1-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc6d1-115">-Name</span></span>
<span data-ttu-id="dc6d1-116">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="dc6d1-116">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6d1-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="dc6d1-117">-PostMigrationName</span></span>
<span data-ttu-id="dc6d1-118">Publicera namn på migrering för standrad namn område i migrering</span><span class="sxs-lookup"><span data-stu-id="dc6d1-118">Post Migration Name for Standrad Namespace in Migration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6d1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc6d1-119">-ResourceGroupName</span></span>
<span data-ttu-id="dc6d1-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="dc6d1-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6d1-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="dc6d1-121">-TargetNameSpace</span></span>
<span data-ttu-id="dc6d1-122">Premium namespace ARM-ID</span><span class="sxs-lookup"><span data-stu-id="dc6d1-122">Premium Namespace ARM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6d1-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dc6d1-123">-Confirm</span></span>
<span data-ttu-id="dc6d1-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6d1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc6d1-125">-WhatIf</span></span>
<span data-ttu-id="dc6d1-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc6d1-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc6d1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc6d1-128">CommonParameters</span></span>
<span data-ttu-id="dc6d1-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc6d1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc6d1-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc6d1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc6d1-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc6d1-131">INPUTS</span></span>

### <span data-ttu-id="dc6d1-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc6d1-132">None</span></span>

## <span data-ttu-id="dc6d1-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc6d1-133">OUTPUTS</span></span>

### <span data-ttu-id="dc6d1-134">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="dc6d1-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="dc6d1-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc6d1-135">NOTES</span></span>

## <span data-ttu-id="dc6d1-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc6d1-136">RELATED LINKS</span></span>
