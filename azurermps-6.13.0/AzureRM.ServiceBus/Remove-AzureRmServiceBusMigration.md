---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576071"
---
# <span data-ttu-id="1497a-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1497a-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="1497a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1497a-102">SYNOPSIS</span></span>
<span data-ttu-id="1497a-103">Cmdlet tar bort migrerings konfigurationen som standard för premie namn områden</span><span class="sxs-lookup"><span data-stu-id="1497a-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1497a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1497a-104">SYNTAX</span></span>

### <span data-ttu-id="1497a-105">MigrationConfigurationPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1497a-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1497a-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1497a-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1497a-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1497a-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1497a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1497a-108">DESCRIPTION</span></span>
<span data-ttu-id="1497a-109">Cmdleten **Remove-AzureRmServiceBusMigration** tar bort migreringsguiden som standard för premie namn områden</span><span class="sxs-lookup"><span data-stu-id="1497a-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="1497a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1497a-110">EXAMPLES</span></span>

### <span data-ttu-id="1497a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1497a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="1497a-112">Tar bort konfigurationen för TestingNamespaceStandardMirgation</span><span class="sxs-lookup"><span data-stu-id="1497a-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="1497a-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1497a-113">PARAMETERS</span></span>

### <span data-ttu-id="1497a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1497a-114">-AsJob</span></span>
<span data-ttu-id="1497a-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1497a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1497a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1497a-116">-DefaultProfile</span></span>
<span data-ttu-id="1497a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1497a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1497a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1497a-118">-InputObject</span></span>
<span data-ttu-id="1497a-119">Service Bus migration standard namn på objekt</span><span class="sxs-lookup"><span data-stu-id="1497a-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="1497a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1497a-120">-Name</span></span>
<span data-ttu-id="1497a-121">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="1497a-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="1497a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1497a-122">-PassThru</span></span>
<span data-ttu-id="1497a-123">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="1497a-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1497a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1497a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1497a-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1497a-125">Resource Group Name</span></span>

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

### <span data-ttu-id="1497a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1497a-126">-ResourceId</span></span>
<span data-ttu-id="1497a-127">Service Bus migration standard resurs-ID för namn område</span><span class="sxs-lookup"><span data-stu-id="1497a-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="1497a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1497a-128">-Confirm</span></span>
<span data-ttu-id="1497a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1497a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1497a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1497a-130">-WhatIf</span></span>
<span data-ttu-id="1497a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1497a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1497a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1497a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1497a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1497a-133">CommonParameters</span></span>
<span data-ttu-id="1497a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1497a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1497a-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1497a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1497a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1497a-136">INPUTS</span></span>

### <span data-ttu-id="1497a-137">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1497a-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="1497a-138">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1497a-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1497a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1497a-139">System.String</span></span>

## <span data-ttu-id="1497a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1497a-140">OUTPUTS</span></span>

### <span data-ttu-id="1497a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1497a-141">System.Boolean</span></span>

## <span data-ttu-id="1497a-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1497a-142">NOTES</span></span>

## <span data-ttu-id="1497a-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1497a-143">RELATED LINKS</span></span>
