---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 3f8b3ad20e9a80344227a28dd7cd1f2763cbaab4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929069"
---
# <span data-ttu-id="91f78-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="91f78-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="91f78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91f78-102">SYNOPSIS</span></span>
<span data-ttu-id="91f78-103">Skapar en ny eller uppdaterar en befintlig åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="91f78-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91f78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91f78-104">SYNTAX</span></span>

### <span data-ttu-id="91f78-105">ByPropertyName (standard)</span><span class="sxs-lookup"><span data-stu-id="91f78-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91f78-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91f78-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91f78-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="91f78-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91f78-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91f78-108">DESCRIPTION</span></span>
<span data-ttu-id="91f78-109">Cmdleten **set-AzureRmActionGroup** skapar en ny eller uppdaterar en befintlig åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="91f78-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="91f78-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91f78-110">EXAMPLES</span></span>

### <span data-ttu-id="91f78-111">Exempel 1: skapa en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="91f78-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="91f78-112">De två första kommandona skapar två mottagare.</span><span class="sxs-lookup"><span data-stu-id="91f78-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="91f78-113">Med kommandot slut skapas en åtgärds grupp, inklusive de två mottagarna.</span><span class="sxs-lookup"><span data-stu-id="91f78-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="91f78-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91f78-114">PARAMETERS</span></span>

### <span data-ttu-id="91f78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f78-115">-DefaultProfile</span></span>
<span data-ttu-id="91f78-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="91f78-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91f78-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="91f78-117">-DisableGroup</span></span>
<span data-ttu-id="91f78-118">Inaktiverar åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="91f78-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91f78-119">-InputObject</span></span>
<span data-ttu-id="91f78-120">Resourc åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="91f78-120">The action group resourc</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="91f78-121">-Name</span></span>
<span data-ttu-id="91f78-122">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="91f78-122">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-123">-Mottagare</span><span class="sxs-lookup"><span data-stu-id="91f78-123">-Receiver</span></span>
<span data-ttu-id="91f78-124">Listan över mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="91f78-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f78-125">-ResourceGroupName</span></span>
<span data-ttu-id="91f78-126">Resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="91f78-126">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91f78-127">-ResourceId</span></span>
<span data-ttu-id="91f78-128">Resursen i</span><span class="sxs-lookup"><span data-stu-id="91f78-128">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="91f78-129">-ShortName</span></span>
<span data-ttu-id="91f78-130">Kort namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="91f78-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="91f78-131">-Tag</span></span>
<span data-ttu-id="91f78-132">Taggarna för instruktions gruppen resourc</span><span class="sxs-lookup"><span data-stu-id="91f78-132">The tags of the action group resourc</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91f78-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91f78-133">-Confirm</span></span>
<span data-ttu-id="91f78-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91f78-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f78-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f78-135">-WhatIf</span></span>
<span data-ttu-id="91f78-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91f78-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91f78-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91f78-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f78-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f78-138">CommonParameters</span></span>
<span data-ttu-id="91f78-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f78-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f78-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91f78-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f78-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91f78-141">INPUTS</span></span>

### <span data-ttu-id="91f78-142">System. String</span><span class="sxs-lookup"><span data-stu-id="91f78-142">System.String</span></span>

### <span data-ttu-id="91f78-143">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. commands. Insights, version = 5.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="91f78-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="91f78-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="91f78-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="91f78-145">System. Collections. Generic. IDictionary ' 2 [[system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089], [system. String, mscorlib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="91f78-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="91f78-146">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="91f78-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="91f78-147">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="91f78-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="91f78-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91f78-148">OUTPUTS</span></span>

### <span data-ttu-id="91f78-149">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="91f78-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="91f78-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91f78-150">NOTES</span></span>

## <span data-ttu-id="91f78-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91f78-151">RELATED LINKS</span></span>

<span data-ttu-id="91f78-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="91f78-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
