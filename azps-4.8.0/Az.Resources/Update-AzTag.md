---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: 4adda2affcba1c29352f6fe9235a5f10a3c1382a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258030"
---
# <span data-ttu-id="cbd69-101">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="cbd69-101">Update-AzTag</span></span>

## <span data-ttu-id="cbd69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbd69-102">SYNOPSIS</span></span>

<span data-ttu-id="cbd69-103">Uppdaterar uppsättningen taggar för en resurs eller ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="cbd69-103">Selectively updates the set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="cbd69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbd69-104">SYNTAX</span></span>

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## <span data-ttu-id="cbd69-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbd69-105">DESCRIPTION</span></span>

<span data-ttu-id="cbd69-106">Cmdleten **Update-AzTag** med en **ResourceID** uppdaterar uppsättningen taggar på en resurs eller ett abonnemang selektivt.</span><span class="sxs-lookup"><span data-stu-id="cbd69-106">The **Update-AzTag** cmdlet with a **ResourceId** selectively updates the set of tags on a resource or subscription.</span></span>
<span data-ttu-id="cbd69-107">Med den här åtgärden kan du ersätta, sammanfoga eller selektivt ta bort taggar för den angivna resursen eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="cbd69-107">This operation allows replacing, merging or selectively deleting tags on the specified resource or subscription.</span></span> <span data-ttu-id="cbd69-108">Den angivna enheten kan innehålla högst 50 taggar efter åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cbd69-108">The specified entity can have a maximum of 50 tags at the end of the operation.</span></span> <span data-ttu-id="cbd69-109">Alternativet Ersätt ersätter hela uppsättningen befintliga taggar med en ny uppsättning.</span><span class="sxs-lookup"><span data-stu-id="cbd69-109">The 'replace' option replaces the entire set of existing tags with a new set.</span></span> <span data-ttu-id="cbd69-110">Med alternativet "koppla" kan du lägga till taggar med nya namn och uppdatera värden för Taggar med befintliga namn.</span><span class="sxs-lookup"><span data-stu-id="cbd69-110">The 'merge' option allows adding tags with new names and updating the values of tags with existing names.</span></span> <span data-ttu-id="cbd69-111">Alternativet "ta bort" tillåter selektiv borttagning av Taggar baserat på angivna namn eller namn/värde-par.</span><span class="sxs-lookup"><span data-stu-id="cbd69-111">The 'delete' option allows selectively deleting tags based on given names or name/value pairs.</span></span>

## <span data-ttu-id="cbd69-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbd69-112">EXAMPLES</span></span>

### <span data-ttu-id="cbd69-113">Exempel 1: uppdatera uppsättningen med taggar i ett abonnemang med "slå samman"</span><span class="sxs-lookup"><span data-stu-id="cbd69-113">Example 1: Selectively updates the set of tags on a subscription with "Merge" Operation</span></span>

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

<span data-ttu-id="cbd69-114">Med det här kommandot kopplas uppsättningen av taggar för abonnemanget med {subId}.</span><span class="sxs-lookup"><span data-stu-id="cbd69-114">This command Merges the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="cbd69-115">Exempel 2: uppdatera uppsättningen med taggar för ett abonnemang med "Ersätt"-åtgärd</span><span class="sxs-lookup"><span data-stu-id="cbd69-115">Example 2: Selectively updates the set of tags on a subscription with "Replace" Operation</span></span>

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

<span data-ttu-id="cbd69-116">Det här kommandot Repalces den uppsättning taggar i prenumerationen med {subId}.</span><span class="sxs-lookup"><span data-stu-id="cbd69-116">This command Repalces the set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="cbd69-117">Exempel 3: uppdatera uppsättningen av taggar i ett abonnemang med åtgärden "ta bort"</span><span class="sxs-lookup"><span data-stu-id="cbd69-117">Example 3: Selectively updates the set of tags on a subscription with "Delete" Operation</span></span>

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

<span data-ttu-id="cbd69-118">Det här kommandot tar bort den uppsättning taggarna för abonnemanget med {subId}.</span><span class="sxs-lookup"><span data-stu-id="cbd69-118">This command Deletes the set of tags on the subscription with {subId}.</span></span>

## <span data-ttu-id="cbd69-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbd69-119">PARAMETERS</span></span>

### <span data-ttu-id="cbd69-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd69-120">-DefaultProfile</span></span>
<span data-ttu-id="cbd69-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd69-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbd69-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbd69-122">-ResourceId</span></span>
<span data-ttu-id="cbd69-123">Resurs-ID för den märkta enheten.</span><span class="sxs-lookup"><span data-stu-id="cbd69-123">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="cbd69-124">En resurs, en resurs grupp eller ett abonnemang kan märkas.</span><span class="sxs-lookup"><span data-stu-id="cbd69-124">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd69-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="cbd69-125">-Tag</span></span>
<span data-ttu-id="cbd69-126">Den uppsättning taggar som ska användas för uppdatering.</span><span class="sxs-lookup"><span data-stu-id="cbd69-126">The set of tags to use for update.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd69-127">-Åtgärd</span><span class="sxs-lookup"><span data-stu-id="cbd69-127">-Operation</span></span>
<span data-ttu-id="cbd69-128">Uppdaterings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="cbd69-128">The update operation.</span></span> <span data-ttu-id="cbd69-129">Alternativen kopplas, Ersätt och ta bort.</span><span class="sxs-lookup"><span data-stu-id="cbd69-129">Options are Merge, Replace and Delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd69-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbd69-130">-Confirm</span></span>
<span data-ttu-id="cbd69-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbd69-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd69-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd69-132">-WhatIf</span></span>
<span data-ttu-id="cbd69-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbd69-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbd69-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbd69-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd69-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd69-135">CommonParameters</span></span>
<span data-ttu-id="cbd69-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd69-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd69-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cbd69-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd69-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbd69-138">INPUTS</span></span>

### <span data-ttu-id="cbd69-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cbd69-139">System.String</span></span>

### <span data-ttu-id="cbd69-140">Microsoft. Azure. commands. taggar. Model. TagPatchOpeation</span><span class="sxs-lookup"><span data-stu-id="cbd69-140">Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation</span></span>

### <span data-ttu-id="cbd69-141">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="cbd69-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cbd69-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbd69-142">OUTPUTS</span></span>

### <span data-ttu-id="cbd69-143">Microsoft. Azure. commands. taggar. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="cbd69-143">Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="cbd69-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbd69-144">NOTES</span></span>

## <span data-ttu-id="cbd69-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbd69-145">RELATED LINKS</span></span>

[<span data-ttu-id="cbd69-146">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="cbd69-146">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="cbd69-147">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="cbd69-147">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="cbd69-148">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="cbd69-148">Remove-AzTag</span></span>](./Remove-AzTag.md)