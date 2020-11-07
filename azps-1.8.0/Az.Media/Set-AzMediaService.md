---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: d035890f6478c0b7fd767f12b8f9a27d4f765837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915753"
---
# <span data-ttu-id="c9365-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c9365-101">Set-AzMediaService</span></span>

## <span data-ttu-id="c9365-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9365-102">SYNOPSIS</span></span>
<span data-ttu-id="c9365-103">Ändrar angivna egenskaper för en befintlig medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="c9365-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="c9365-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9365-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9365-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9365-105">DESCRIPTION</span></span>
<span data-ttu-id="c9365-106">Cmdleten **set-AzMediaService** ändrar angivna egenskaper för en befintlig medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="c9365-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="c9365-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9365-107">EXAMPLES</span></span>

### <span data-ttu-id="c9365-108">Exempel 1: ändra en befintlig medie tjänst</span><span class="sxs-lookup"><span data-stu-id="c9365-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="c9365-109">Det första kommandot skapar en serie Taggar och lagrar taggarna i variabeln som heter $Tags.</span><span class="sxs-lookup"><span data-stu-id="c9365-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="c9365-110">Det här andra kommandot uppdaterar medie tjänsten med namnet MediaService001 som tillhör resurs gruppen med namnet ResourceGroup123 med taggarna i $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="c9365-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="c9365-111">Kommandot använder också en matris med lagrings konfigurations objekt som lagras i $StorageAccounts variabel.</span><span class="sxs-lookup"><span data-stu-id="c9365-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="c9365-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9365-112">PARAMETERS</span></span>

### <span data-ttu-id="c9365-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c9365-113">-AccountName</span></span>
<span data-ttu-id="c9365-114">Anger namnet på den medie tjänst som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="c9365-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9365-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9365-115">-DefaultProfile</span></span>
<span data-ttu-id="c9365-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c9365-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9365-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9365-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9365-118">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9365-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9365-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="c9365-119">-StorageAccounts</span></span>
<span data-ttu-id="c9365-120">Anger en matris med lagrings konton som denna cmdlet associerar med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="c9365-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9365-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c9365-121">-Tag</span></span>
<span data-ttu-id="c9365-122">De taggar som är kopplade till medie kontot.</span><span class="sxs-lookup"><span data-stu-id="c9365-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9365-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9365-123">-Confirm</span></span>
<span data-ttu-id="c9365-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c9365-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9365-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9365-125">-WhatIf</span></span>
<span data-ttu-id="c9365-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c9365-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9365-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c9365-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9365-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9365-128">CommonParameters</span></span>
<span data-ttu-id="c9365-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9365-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9365-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9365-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9365-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9365-131">INPUTS</span></span>

### <span data-ttu-id="c9365-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c9365-132">System.String</span></span>

### <span data-ttu-id="c9365-133">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="c9365-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c9365-134">Microsoft. Azure. commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="c9365-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="c9365-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9365-135">OUTPUTS</span></span>

### <span data-ttu-id="c9365-136">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="c9365-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="c9365-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9365-137">NOTES</span></span>

## <span data-ttu-id="c9365-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9365-138">RELATED LINKS</span></span>

[<span data-ttu-id="c9365-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c9365-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="c9365-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c9365-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="c9365-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c9365-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


