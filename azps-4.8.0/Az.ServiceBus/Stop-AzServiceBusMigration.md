---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100823"
---
# <span data-ttu-id="04584-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="04584-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="04584-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04584-102">SYNOPSIS</span></span>
<span data-ttu-id="04584-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="04584-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="04584-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04584-104">SYNTAX</span></span>

### <span data-ttu-id="04584-105">MigrationConfigurationPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="04584-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04584-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="04584-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04584-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04584-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04584-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04584-108">DESCRIPTION</span></span>
<span data-ttu-id="04584-109">Cmdleten **Stop-AzServiceBusMigration** avbryter migreringen mellan standard och Premium-namnrymd</span><span class="sxs-lookup"><span data-stu-id="04584-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="04584-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04584-110">EXAMPLES</span></span>

### <span data-ttu-id="04584-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04584-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="04584-112">Cmdlet avbryter migreringen mellan standard namn området och Premium-namn området som tillhandahålls när migreringsguiden skapades.</span><span class="sxs-lookup"><span data-stu-id="04584-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="04584-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04584-113">PARAMETERS</span></span>

### <span data-ttu-id="04584-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04584-114">-DefaultProfile</span></span>
<span data-ttu-id="04584-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04584-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04584-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04584-116">-InputObject</span></span>
<span data-ttu-id="04584-117">Konfiguration av Service Bus migration standard namn område för objekt</span><span class="sxs-lookup"><span data-stu-id="04584-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="04584-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="04584-118">-Name</span></span>
<span data-ttu-id="04584-119">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="04584-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="04584-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04584-120">-PassThru</span></span>
<span data-ttu-id="04584-121">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="04584-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="04584-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04584-122">-ResourceGroupName</span></span>
<span data-ttu-id="04584-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="04584-123">Resource Group Name</span></span>

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

### <span data-ttu-id="04584-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04584-124">-ResourceId</span></span>
<span data-ttu-id="04584-125">Konfiguration av Service Bus-migrering standard namn på namespace-resurs</span><span class="sxs-lookup"><span data-stu-id="04584-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="04584-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04584-126">-Confirm</span></span>
<span data-ttu-id="04584-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04584-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04584-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04584-128">-WhatIf</span></span>
<span data-ttu-id="04584-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04584-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04584-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04584-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04584-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04584-131">CommonParameters</span></span>
<span data-ttu-id="04584-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04584-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04584-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04584-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04584-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04584-134">INPUTS</span></span>

### <span data-ttu-id="04584-135">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="04584-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="04584-136">System. String</span><span class="sxs-lookup"><span data-stu-id="04584-136">System.String</span></span>

## <span data-ttu-id="04584-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04584-137">OUTPUTS</span></span>

### <span data-ttu-id="04584-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04584-138">System.Boolean</span></span>

## <span data-ttu-id="04584-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04584-139">NOTES</span></span>

## <span data-ttu-id="04584-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04584-140">RELATED LINKS</span></span>
