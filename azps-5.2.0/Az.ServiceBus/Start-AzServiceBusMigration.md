---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/start-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Start-AzServiceBusMigration.md
ms.openlocfilehash: 0837532c6e708b4ff7d8cbee4f5ad231b4032347
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415963"
---
# <span data-ttu-id="d1101-101">Start-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="d1101-101">Start-AzServiceBusMigration</span></span>

## <span data-ttu-id="d1101-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1101-102">SYNOPSIS</span></span>
<span data-ttu-id="d1101-103">Skapar en ny migrering och börjar migrera enheter från standard till premie namn områden</span><span class="sxs-lookup"><span data-stu-id="d1101-103">Creates a new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="d1101-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1101-104">SYNTAX</span></span>

```
Start-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-TargetNameSpace] <String>
 [-PostMigrationName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1101-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1101-105">DESCRIPTION</span></span>
<span data-ttu-id="d1101-106">Cmdleten **Start-AzServiceBusMigration** skapar en ny migrering och börjar migrera enheter från standard till premie namn områden</span><span class="sxs-lookup"><span data-stu-id="d1101-106">The **Start-AzServiceBusMigration** cmdlet creates an new Migration configuration and starts migrating entities from Standard to Premium namespaces</span></span>

## <span data-ttu-id="d1101-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1101-107">EXAMPLES</span></span>

### <span data-ttu-id="d1101-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d1101-108">Example 1</span></span>
```powershell
PS C:\> Start-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration -TargetNameSpace /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration -PostMigrationName TestingNamespaceStandardMigrationPostMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Accepted
TargetNamespace   : /subscriptions/SubscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="d1101-109">Skapar en ny migrerings konfiguration för ' TestingNamespaceStandardMigration ' till ' TestingNamespacePremiumMigration '-namn områden</span><span class="sxs-lookup"><span data-stu-id="d1101-109">Creates a new migration configuration for 'TestingNamespaceStandardMigration' to 'TestingNamespacePremiumMigration' namespaces</span></span>

## <span data-ttu-id="d1101-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1101-110">PARAMETERS</span></span>

### <span data-ttu-id="d1101-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1101-111">-AsJob</span></span>
<span data-ttu-id="d1101-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d1101-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1101-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1101-113">-DefaultProfile</span></span>
<span data-ttu-id="d1101-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1101-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1101-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d1101-115">-Name</span></span>
<span data-ttu-id="d1101-116">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="d1101-116">Standard Namespace Name</span></span>

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

### <span data-ttu-id="d1101-117">-PostMigrationName</span><span class="sxs-lookup"><span data-stu-id="d1101-117">-PostMigrationName</span></span>
<span data-ttu-id="d1101-118">Namn på migrering för standard namn område i migrering</span><span class="sxs-lookup"><span data-stu-id="d1101-118">Post Migration Name for Standard Namespace in Migration</span></span>

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

### <span data-ttu-id="d1101-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1101-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1101-120">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d1101-120">Resource Group Name</span></span>

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

### <span data-ttu-id="d1101-121">-TargetNameSpace</span><span class="sxs-lookup"><span data-stu-id="d1101-121">-TargetNameSpace</span></span>
<span data-ttu-id="d1101-122">Premium namespace ARM-ID</span><span class="sxs-lookup"><span data-stu-id="d1101-122">Premium Namespace ARM Id</span></span>

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

### <span data-ttu-id="d1101-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1101-123">-Confirm</span></span>
<span data-ttu-id="d1101-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1101-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1101-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1101-125">-WhatIf</span></span>
<span data-ttu-id="d1101-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1101-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1101-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1101-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1101-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1101-128">CommonParameters</span></span>
<span data-ttu-id="d1101-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1101-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1101-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1101-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1101-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1101-131">INPUTS</span></span>

### <span data-ttu-id="d1101-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="d1101-132">None</span></span>

## <span data-ttu-id="d1101-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1101-133">OUTPUTS</span></span>

### <span data-ttu-id="d1101-134">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="d1101-134">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="d1101-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1101-135">NOTES</span></span>

## <span data-ttu-id="d1101-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1101-136">RELATED LINKS</span></span>
