---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: b4f509d6ba688cab993f83cd0b094b3f8394d36f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574287"
---
# <span data-ttu-id="63897-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="63897-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="63897-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63897-102">SYNOPSIS</span></span>
<span data-ttu-id="63897-103">Skapar en ny eller uppdaterar en befintlig åtgärds grupp.</span><span class="sxs-lookup"><span data-stu-id="63897-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63897-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63897-104">SYNTAX</span></span>

### <span data-ttu-id="63897-105">ByPropertyName (standard)</span><span class="sxs-lookup"><span data-stu-id="63897-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63897-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63897-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63897-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="63897-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63897-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63897-108">DESCRIPTION</span></span>
<span data-ttu-id="63897-109">Cmdleten **set-AzureRmActionGroup** skapar en ny eller uppdaterar en befintlig åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="63897-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="63897-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63897-110">EXAMPLES</span></span>

### <span data-ttu-id="63897-111">Exempel 1: skapa en åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="63897-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="63897-112">De två första kommandona skapar två mottagare.</span><span class="sxs-lookup"><span data-stu-id="63897-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="63897-113">Med kommandot slut skapas en åtgärds grupp, inklusive de två mottagarna.</span><span class="sxs-lookup"><span data-stu-id="63897-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="63897-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63897-114">PARAMETERS</span></span>

### <span data-ttu-id="63897-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63897-115">-DefaultProfile</span></span>
<span data-ttu-id="63897-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="63897-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63897-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="63897-117">-DisableGroup</span></span>
<span data-ttu-id="63897-118">Inaktiverar åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="63897-118">Disables the action group.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63897-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63897-119">-InputObject</span></span>
<span data-ttu-id="63897-120">Resourc åtgärds grupp</span><span class="sxs-lookup"><span data-stu-id="63897-120">The action group resourc</span></span>

```yaml
Type: PSActionGroupResource
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63897-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="63897-121">-Name</span></span>
<span data-ttu-id="63897-122">Namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="63897-122">The name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63897-123">-Mottagare</span><span class="sxs-lookup"><span data-stu-id="63897-123">-Receiver</span></span>
<span data-ttu-id="63897-124">Listan över mottagare av åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="63897-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="63897-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63897-125">-ResourceGroupName</span></span>
<span data-ttu-id="63897-126">Resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="63897-126">The resource group nam</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63897-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63897-127">-ResourceId</span></span>
<span data-ttu-id="63897-128">Resursen i</span><span class="sxs-lookup"><span data-stu-id="63897-128">The resource i</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63897-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="63897-129">-ShortName</span></span>
<span data-ttu-id="63897-130">Kort namnet på åtgärds gruppen.</span><span class="sxs-lookup"><span data-stu-id="63897-130">The short name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: ByPropertyName, ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63897-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="63897-131">-Tag</span></span>
<span data-ttu-id="63897-132">Taggarna för instruktions gruppen resourc</span><span class="sxs-lookup"><span data-stu-id="63897-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="63897-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63897-133">-Confirm</span></span>
<span data-ttu-id="63897-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63897-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63897-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63897-135">-WhatIf</span></span>
<span data-ttu-id="63897-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63897-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63897-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63897-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63897-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63897-138">CommonParameters</span></span>
<span data-ttu-id="63897-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63897-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63897-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63897-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63897-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63897-141">INPUTS</span></span>

### <span data-ttu-id="63897-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="63897-142">None</span></span>
<span data-ttu-id="63897-143">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="63897-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63897-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63897-144">OUTPUTS</span></span>

### <span data-ttu-id="63897-145">Microsoft. Azure. commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="63897-145">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="63897-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63897-146">NOTES</span></span>

## <span data-ttu-id="63897-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63897-147">RELATED LINKS</span></span>

<span data-ttu-id="63897-148">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="63897-148">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
