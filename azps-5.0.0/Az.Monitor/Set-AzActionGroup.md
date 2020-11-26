---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: b10aad8cdf480dd567b0646fb3befa95fb32bf72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270848"
---
# <span data-ttu-id="17806-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="17806-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="17806-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17806-102">SYNOPSIS</span></span>
<span data-ttu-id="17806-103">Skapar en ny eller uppdaterar en befintlig åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="17806-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="17806-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17806-104">SYNTAX</span></span>

### <span data-ttu-id="17806-105">ByPropertyName (standard)</span><span class="sxs-lookup"><span data-stu-id="17806-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17806-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17806-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17806-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="17806-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17806-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17806-108">DESCRIPTION</span></span>
<span data-ttu-id="17806-109">Cmdleten **set-AzActionGroup** skapar en ny eller uppdaterar en befintlig åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="17806-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="17806-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17806-110">EXAMPLES</span></span>

### <span data-ttu-id="17806-111">Exempel 1: skapa en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="17806-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="17806-112">De två första kommandona skapar två mottagare.</span><span class="sxs-lookup"><span data-stu-id="17806-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="17806-113">Med kommandot slut skapas en åtgärds grupp, inklusive de två mottagarna.</span><span class="sxs-lookup"><span data-stu-id="17806-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="17806-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17806-114">PARAMETERS</span></span>

### <span data-ttu-id="17806-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17806-115">-DefaultProfile</span></span>
<span data-ttu-id="17806-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="17806-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17806-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="17806-117">-DisableGroup</span></span>
<span data-ttu-id="17806-118">Inaktiverar åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="17806-118">Disables the action group.</span></span>

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

### <span data-ttu-id="17806-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17806-119">-InputObject</span></span>
<span data-ttu-id="17806-120">Resurs för åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="17806-120">The action group resource</span></span>

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

### <span data-ttu-id="17806-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="17806-121">-Name</span></span>
<span data-ttu-id="17806-122">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="17806-122">The name of the action group.</span></span>

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

### <span data-ttu-id="17806-123">-Mottagare</span><span class="sxs-lookup"><span data-stu-id="17806-123">-Receiver</span></span>
<span data-ttu-id="17806-124">Listan över mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="17806-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="17806-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17806-125">-ResourceGroupName</span></span>
<span data-ttu-id="17806-126">Resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="17806-126">The resource group nam</span></span>

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

### <span data-ttu-id="17806-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17806-127">-ResourceId</span></span>
<span data-ttu-id="17806-128">Resursen i</span><span class="sxs-lookup"><span data-stu-id="17806-128">The resource i</span></span>

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

### <span data-ttu-id="17806-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="17806-129">-ShortName</span></span>
<span data-ttu-id="17806-130">Kort namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="17806-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="17806-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="17806-131">-Tag</span></span>
<span data-ttu-id="17806-132">Taggarna för åtgärds grupp resursen</span><span class="sxs-lookup"><span data-stu-id="17806-132">The tags of the action group resource</span></span>

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

### <span data-ttu-id="17806-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17806-133">-Confirm</span></span>
<span data-ttu-id="17806-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17806-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17806-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17806-135">-WhatIf</span></span>
<span data-ttu-id="17806-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17806-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17806-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17806-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17806-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17806-138">CommonParameters</span></span>
<span data-ttu-id="17806-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17806-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17806-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17806-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17806-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17806-141">INPUTS</span></span>

### <span data-ttu-id="17806-142">System. String</span><span class="sxs-lookup"><span data-stu-id="17806-142">System.String</span></span>

### <span data-ttu-id="17806-143">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. cmdletar. Monitor, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="17806-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="17806-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="17806-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="17806-145">System. Collections. Generic. IDictionary ' 2 [[system. String, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e], [system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17806-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="17806-146">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="17806-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="17806-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17806-147">OUTPUTS</span></span>

### <span data-ttu-id="17806-148">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="17806-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="17806-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17806-149">NOTES</span></span>

## <span data-ttu-id="17806-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17806-150">RELATED LINKS</span></span>

<span data-ttu-id="17806-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="17806-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>