---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/stop-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
ms.openlocfilehash: 25a8b6918c5cd10a2f47230274c357008731ffba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577884"
---
# <span data-ttu-id="fd594-101">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="fd594-101">Stop-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="fd594-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd594-102">SYNOPSIS</span></span>
<span data-ttu-id="fd594-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="fd594-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd594-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd594-104">SYNTAX</span></span>

### <span data-ttu-id="fd594-105">MigrationConfigurationPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fd594-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd594-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd594-106">NamespaceInputObjectSet</span></span>
```
Stop-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd594-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd594-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd594-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd594-108">DESCRIPTION</span></span>
<span data-ttu-id="fd594-109">Cmdleten **Stop-AzureRmServiceBusMigration** Tremitates över gången mellan standard och Premium-namnrymd</span><span class="sxs-lookup"><span data-stu-id="fd594-109">The **Stop-AzureRmServiceBusMigration** cmdlets  tremitates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="fd594-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd594-110">EXAMPLES</span></span>

### <span data-ttu-id="fd594-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fd594-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="fd594-112">cmdlet termitates migreringen mellan standard namn området och Premium-namn området som tillhandahålls när migreringen skapades.</span><span class="sxs-lookup"><span data-stu-id="fd594-112">cmdlet termitates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="fd594-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd594-113">PARAMETERS</span></span>

### <span data-ttu-id="fd594-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd594-114">-DefaultProfile</span></span>
<span data-ttu-id="fd594-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd594-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd594-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd594-116">-InputObject</span></span>
<span data-ttu-id="fd594-117">Konfiguration av Service Bus migration standard namn område för objekt</span><span class="sxs-lookup"><span data-stu-id="fd594-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd594-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="fd594-118">-Name</span></span>
<span data-ttu-id="fd594-119">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="fd594-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="fd594-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd594-120">-PassThru</span></span>
<span data-ttu-id="fd594-121">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="fd594-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="fd594-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd594-122">-ResourceGroupName</span></span>
<span data-ttu-id="fd594-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fd594-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd594-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd594-124">-ResourceId</span></span>
<span data-ttu-id="fd594-125">Konfiguration av Service Bus-migrering standard namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="fd594-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd594-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fd594-126">-Confirm</span></span>
<span data-ttu-id="fd594-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fd594-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd594-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd594-128">-WhatIf</span></span>
<span data-ttu-id="fd594-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fd594-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd594-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fd594-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd594-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd594-131">CommonParameters</span></span>
<span data-ttu-id="fd594-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd594-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd594-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd594-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd594-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd594-134">INPUTS</span></span>

### <span data-ttu-id="fd594-135">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="fd594-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="fd594-136">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd594-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="fd594-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fd594-137">System.String</span></span>

## <span data-ttu-id="fd594-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd594-138">OUTPUTS</span></span>

### <span data-ttu-id="fd594-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd594-139">System.Boolean</span></span>

## <span data-ttu-id="fd594-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd594-140">NOTES</span></span>

## <span data-ttu-id="fd594-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd594-141">RELATED LINKS</span></span>
