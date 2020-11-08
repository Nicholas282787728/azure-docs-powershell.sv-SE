---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 0b8290a9cb782ee3801e34e55fef1997a4745aee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919222"
---
# <span data-ttu-id="7e177-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="7e177-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="7e177-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e177-102">SYNOPSIS</span></span>
<span data-ttu-id="7e177-103">Cmdletar ställer in migreringen från standard till Premium-namnrymd som fullständig och anslutnings strängar med standard namn område pekar nu på Premium-namnrymd</span><span class="sxs-lookup"><span data-stu-id="7e177-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="7e177-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e177-104">SYNTAX</span></span>

### <span data-ttu-id="7e177-105">MigrationConfigurationPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7e177-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e177-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7e177-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e177-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e177-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e177-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e177-108">DESCRIPTION</span></span>
<span data-ttu-id="7e177-109">Cmdleten **Complete-AzServiceBusMigration** ställer in migreringen från standard till Premium-namnrymd som fullständig och anslutnings strängar med standard namn område pekar nu på Premium-namnrymd</span><span class="sxs-lookup"><span data-stu-id="7e177-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="7e177-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e177-110">EXAMPLES</span></span>

### <span data-ttu-id="7e177-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7e177-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="7e177-112">Anger migreringen av ' NamespaceStandardMigration ' s namn område som slutfört.</span><span class="sxs-lookup"><span data-stu-id="7e177-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="7e177-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e177-113">PARAMETERS</span></span>

### <span data-ttu-id="7e177-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e177-114">-DefaultProfile</span></span>
<span data-ttu-id="7e177-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e177-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e177-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e177-116">-InputObject</span></span>
<span data-ttu-id="7e177-117">Konfiguration av Service Bus-migrering-standard namn på objekt</span><span class="sxs-lookup"><span data-stu-id="7e177-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="7e177-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e177-118">-Name</span></span>
<span data-ttu-id="7e177-119">Namn på standard namn området</span><span class="sxs-lookup"><span data-stu-id="7e177-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="7e177-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e177-120">-PassThru</span></span>
<span data-ttu-id="7e177-121">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="7e177-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7e177-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e177-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e177-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7e177-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7e177-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e177-124">-ResourceId</span></span>
<span data-ttu-id="7e177-125">Service Bus-migrering-standard namn för namespace</span><span class="sxs-lookup"><span data-stu-id="7e177-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="7e177-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e177-126">-Confirm</span></span>
<span data-ttu-id="7e177-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e177-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e177-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e177-128">-WhatIf</span></span>
<span data-ttu-id="7e177-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e177-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e177-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e177-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e177-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e177-131">CommonParameters</span></span>
<span data-ttu-id="7e177-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e177-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e177-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e177-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e177-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e177-134">INPUTS</span></span>

### <span data-ttu-id="7e177-135">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="7e177-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="7e177-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7e177-136">System.String</span></span>

## <span data-ttu-id="7e177-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e177-137">OUTPUTS</span></span>

### <span data-ttu-id="7e177-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e177-138">System.Boolean</span></span>

## <span data-ttu-id="7e177-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e177-139">NOTES</span></span>

## <span data-ttu-id="7e177-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e177-140">RELATED LINKS</span></span>