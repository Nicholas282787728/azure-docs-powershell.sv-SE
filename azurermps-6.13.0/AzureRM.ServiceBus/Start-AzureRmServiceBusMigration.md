---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/start-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Start-AzureRmServiceBusMigration.md
ms.openlocfilehash: 979db64fb11b4fffc901d96811b24be5c79f6b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577899"
---
# <span data-ttu-id="4e274-101">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4e274-101">Start-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="4e274-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e274-102">SYNOPSIS</span></span>
<span data-ttu-id="4e274-103">Skapar en ny migrering och börjar migrera enheter från standard till premie namn områden</span><span class="sxs-lookup"><span data-stu-id="4e274-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e274-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e274-104">SYNTAX</span></span>

```
Start-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e274-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e274-105">DESCRIPTION</span></span>
<span data-ttu-id="4e274-106">Cmdleten **Start-AzureRmServiceBusMigration** skapar en ny migrering och börjar migrera enheter från standard till premie namn områden</span><span class="sxs-lookup"><span data-stu-id="4e274-106">The **Start-AzureRmServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="4e274-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e274-107">EXAMPLES</span></span>

### <span data-ttu-id="4e274-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4e274-108">Example 1</span></span>
```powershell
PS C:\> Start-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation -PostMigrationName TestingNamespaceStandardMirgationPostMigration

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="4e274-109">Skapar en ny migrerings konfiguration för ' TestingNamespaceStandardMirgation ' till ' TestingNamespacePremiumMirgation '-namn områden</span><span class="sxs-lookup"><span data-stu-id="4e274-109">Creates a new migration configuration for 'TestingNamespaceStandardMirgation' to 'TestingNamespacePremiumMirgation' namespaces</span></span>

## <span data-ttu-id="4e274-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e274-110">PARAMETERS</span></span>

### <span data-ttu-id="4e274-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e274-111">-AsJob</span></span>
<span data-ttu-id="4e274-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4e274-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4e274-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e274-113">-DefaultProfile</span></span>
<span data-ttu-id="4e274-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e274-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e274-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e274-115">-Name</span></span>
<span data-ttu-id="4e274-116">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="4e274-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="4e274-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="4e274-117">-PostMigrationName</span></span>
<span data-ttu-id="4e274-118">Publicera namn på migrering för standrad namn område i migrering</span><span class="sxs-lookup"><span data-stu-id="4e274-118">Post Migration Name for Standrad Namespace in Migration</span></span>

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

### <span data-ttu-id="4e274-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e274-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e274-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4e274-120">Resource Group Name</span></span>

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

### <span data-ttu-id="4e274-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="4e274-121">-TargetNameSpace</span></span>
<span data-ttu-id="4e274-122">Premium namespace ARM-ID</span><span class="sxs-lookup"><span data-stu-id="4e274-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="4e274-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e274-123">-Confirm</span></span>
<span data-ttu-id="4e274-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e274-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e274-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e274-125">-WhatIf</span></span>
<span data-ttu-id="4e274-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4e274-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e274-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4e274-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e274-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e274-128">CommonParameters</span></span>
<span data-ttu-id="4e274-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e274-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e274-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e274-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e274-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e274-131">INPUTS</span></span>

### <span data-ttu-id="4e274-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="4e274-132">None</span></span>

## <span data-ttu-id="4e274-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e274-133">OUTPUTS</span></span>

### <span data-ttu-id="4e274-134">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="4e274-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="4e274-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e274-135">NOTES</span></span>

## <span data-ttu-id="4e274-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e274-136">RELATED LINKS</span></span>
