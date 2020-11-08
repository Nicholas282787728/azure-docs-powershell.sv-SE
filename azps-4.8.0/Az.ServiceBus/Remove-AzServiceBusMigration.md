---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259879"
---
# <span data-ttu-id="838f6-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="838f6-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="838f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="838f6-102">SYNOPSIS</span></span>
<span data-ttu-id="838f6-103">Cmdlet tar bort migrerings konfigurationen som standard för premie namn områden</span><span class="sxs-lookup"><span data-stu-id="838f6-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="838f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="838f6-104">SYNTAX</span></span>

### <span data-ttu-id="838f6-105">MigrationConfigurationPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="838f6-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838f6-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="838f6-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="838f6-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="838f6-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="838f6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="838f6-108">DESCRIPTION</span></span>
<span data-ttu-id="838f6-109">Cmdleten **Remove-AzServiceBusMigration** tar bort migreringsguiden som standard för premie namn områden</span><span class="sxs-lookup"><span data-stu-id="838f6-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="838f6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="838f6-110">EXAMPLES</span></span>

### <span data-ttu-id="838f6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="838f6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="838f6-112">Tar bort konfigurationen för TestingNamespaceStandardMigration</span><span class="sxs-lookup"><span data-stu-id="838f6-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="838f6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="838f6-113">PARAMETERS</span></span>

### <span data-ttu-id="838f6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="838f6-114">-AsJob</span></span>
<span data-ttu-id="838f6-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="838f6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="838f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="838f6-116">-DefaultProfile</span></span>
<span data-ttu-id="838f6-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="838f6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="838f6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="838f6-118">-InputObject</span></span>
<span data-ttu-id="838f6-119">Service Bus migration standard namn på objekt</span><span class="sxs-lookup"><span data-stu-id="838f6-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="838f6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="838f6-120">-Name</span></span>
<span data-ttu-id="838f6-121">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="838f6-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="838f6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="838f6-122">-PassThru</span></span>
<span data-ttu-id="838f6-123">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="838f6-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="838f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="838f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="838f6-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="838f6-125">Resource Group Name</span></span>

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

### <span data-ttu-id="838f6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="838f6-126">-ResourceId</span></span>
<span data-ttu-id="838f6-127">Service Bus migration standard resurs-ID för namn område</span><span class="sxs-lookup"><span data-stu-id="838f6-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="838f6-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="838f6-128">-Confirm</span></span>
<span data-ttu-id="838f6-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="838f6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="838f6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="838f6-130">-WhatIf</span></span>
<span data-ttu-id="838f6-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="838f6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="838f6-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="838f6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="838f6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="838f6-133">CommonParameters</span></span>
<span data-ttu-id="838f6-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="838f6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="838f6-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="838f6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="838f6-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="838f6-136">INPUTS</span></span>

### <span data-ttu-id="838f6-137">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="838f6-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="838f6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="838f6-138">System.String</span></span>

## <span data-ttu-id="838f6-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="838f6-139">OUTPUTS</span></span>

### <span data-ttu-id="838f6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="838f6-140">System.Boolean</span></span>

## <span data-ttu-id="838f6-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="838f6-141">NOTES</span></span>

## <span data-ttu-id="838f6-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="838f6-142">RELATED LINKS</span></span>
