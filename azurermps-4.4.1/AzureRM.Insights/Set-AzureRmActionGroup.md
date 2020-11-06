---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: 29ef822e61c13d3ea976002c465a7c114296da9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581420"
---
# <span data-ttu-id="b54e0-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b54e0-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="b54e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b54e0-102">SYNOPSIS</span></span>
<span data-ttu-id="b54e0-103">Skapar en ny eller uppdaterar en befintlig åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="b54e0-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b54e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b54e0-104">SYNTAX</span></span>

### <span data-ttu-id="b54e0-105">ByPropertyName (standard)</span><span class="sxs-lookup"><span data-stu-id="b54e0-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b54e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b54e0-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b54e0-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b54e0-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b54e0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b54e0-108">DESCRIPTION</span></span>
<span data-ttu-id="b54e0-109">Cmdleten **set-AzureRmActionGroup** skapar en ny eller uppdaterar en befintlig åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="b54e0-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="b54e0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b54e0-110">EXAMPLES</span></span>

### <span data-ttu-id="b54e0-111">Exempel 1: skapa en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="b54e0-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="b54e0-112">De två första kommandona skapar två mottagare.</span><span class="sxs-lookup"><span data-stu-id="b54e0-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="b54e0-113">Med kommandot slut skapas en åtgärds grupp, inklusive de två mottagarna.</span><span class="sxs-lookup"><span data-stu-id="b54e0-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="b54e0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b54e0-114">PARAMETERS</span></span>

### <span data-ttu-id="b54e0-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b54e0-115">-Name</span></span>
<span data-ttu-id="b54e0-116">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="b54e0-116">The name of the action group.</span></span>

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

### <span data-ttu-id="b54e0-117">-ShortName</span><span class="sxs-lookup"><span data-stu-id="b54e0-117">-ShortName</span></span>
<span data-ttu-id="b54e0-118">Kort namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="b54e0-118">The short name of the action group.</span></span>

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

### <span data-ttu-id="b54e0-119">-Mottagare</span><span class="sxs-lookup"><span data-stu-id="b54e0-119">-Receiver</span></span>
<span data-ttu-id="b54e0-120">Listan över mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="b54e0-120">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="b54e0-121">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="b54e0-121">-DisableGroup</span></span>
<span data-ttu-id="b54e0-122">Inaktiverar åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="b54e0-122">Disables the action group.</span></span>

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

### <span data-ttu-id="b54e0-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b54e0-123">-Confirm</span></span>
<span data-ttu-id="b54e0-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b54e0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b54e0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54e0-125">-DefaultProfile</span></span>
<span data-ttu-id="b54e0-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b54e0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b54e0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b54e0-127">-InputObject</span></span>
<span data-ttu-id="b54e0-128">Resurs för åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="b54e0-128">The action group resource</span></span>

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

### <span data-ttu-id="b54e0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b54e0-129">-ResourceGroupName</span></span>
<span data-ttu-id="b54e0-130">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="b54e0-130">The resource group name</span></span>

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

### <span data-ttu-id="b54e0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b54e0-131">-ResourceId</span></span>
<span data-ttu-id="b54e0-132">Resurs-ID</span><span class="sxs-lookup"><span data-stu-id="b54e0-132">The resource id</span></span>

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

### <span data-ttu-id="b54e0-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b54e0-133">-Tag</span></span>
<span data-ttu-id="b54e0-134">Taggarna för åtgärds grupp resursen</span><span class="sxs-lookup"><span data-stu-id="b54e0-134">The tags of the action group resource</span></span>

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

### <span data-ttu-id="b54e0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b54e0-135">-WhatIf</span></span>
<span data-ttu-id="b54e0-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b54e0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b54e0-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b54e0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b54e0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54e0-138">CommonParameters</span></span>
<span data-ttu-id="b54e0-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54e0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54e0-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b54e0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54e0-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b54e0-141">INPUTS</span></span>

## <span data-ttu-id="b54e0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b54e0-142">OUTPUTS</span></span>

### <span data-ttu-id="b54e0-143">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="b54e0-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="b54e0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b54e0-144">NOTES</span></span>

## <span data-ttu-id="b54e0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b54e0-145">RELATED LINKS</span></span>

<span data-ttu-id="b54e0-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="b54e0-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
