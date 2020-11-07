---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/complete-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
ms.openlocfilehash: 0006e4768dc27994d18e93e48696b5ee9a514c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757029"
---
# <span data-ttu-id="c8887-101">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c8887-101">Complete-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="c8887-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8887-102">SYNOPSIS</span></span>
<span data-ttu-id="c8887-103">Cmdletar ställer in migreringen från standard till Premium-namnrymd som fullständig och anslutnings strängar med standard namn område pekar nu på Premium-namnrymd</span><span class="sxs-lookup"><span data-stu-id="c8887-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8887-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8887-104">SYNTAX</span></span>

### <span data-ttu-id="c8887-105">MigrationConfigurationPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c8887-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8887-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c8887-106">NamespaceInputObjectSet</span></span>
```
Complete-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8887-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8887-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8887-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8887-108">DESCRIPTION</span></span>
<span data-ttu-id="c8887-109">Cmdleten **Complete-AzureRmServiceBusMigration** ställer in migreringen från standard till Premium-namnrymd som fullständig och anslutnings strängar med standard namn område pekar nu på Premium-namnrymd</span><span class="sxs-lookup"><span data-stu-id="c8887-109">The **Complete-AzureRmServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="c8887-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8887-110">EXAMPLES</span></span>

### <span data-ttu-id="c8887-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c8887-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="c8887-112">Anger migreringen av ' NamespaceStandardMirgation ' s namn område som slutfört.</span><span class="sxs-lookup"><span data-stu-id="c8887-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="c8887-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8887-113">PARAMETERS</span></span>

### <span data-ttu-id="c8887-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8887-114">-DefaultProfile</span></span>
<span data-ttu-id="c8887-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8887-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8887-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8887-116">-InputObject</span></span>
<span data-ttu-id="c8887-117">Konfiguration av Service Bus-migrering-standard namn på objekt</span><span class="sxs-lookup"><span data-stu-id="c8887-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="c8887-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8887-118">-Name</span></span>
<span data-ttu-id="c8887-119">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="c8887-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="c8887-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8887-120">-PassThru</span></span>
<span data-ttu-id="c8887-121">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="c8887-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c8887-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8887-122">-ResourceGroupName</span></span>
<span data-ttu-id="c8887-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c8887-123">Resource Group Name</span></span>

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

### <span data-ttu-id="c8887-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8887-124">-ResourceId</span></span>
<span data-ttu-id="c8887-125">Service Bus Migratio-standard namn områdes resurs-ID</span><span class="sxs-lookup"><span data-stu-id="c8887-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="c8887-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8887-126">-Confirm</span></span>
<span data-ttu-id="c8887-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8887-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8887-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8887-128">-WhatIf</span></span>
<span data-ttu-id="c8887-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8887-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8887-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8887-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8887-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8887-131">CommonParameters</span></span>
<span data-ttu-id="c8887-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8887-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8887-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8887-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8887-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8887-134">INPUTS</span></span>

### <span data-ttu-id="c8887-135">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c8887-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="c8887-136">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8887-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c8887-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c8887-137">System.String</span></span>

## <span data-ttu-id="c8887-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8887-138">OUTPUTS</span></span>

### <span data-ttu-id="c8887-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8887-139">System.Boolean</span></span>

## <span data-ttu-id="c8887-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8887-140">NOTES</span></span>

## <span data-ttu-id="c8887-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8887-141">RELATED LINKS</span></span>
