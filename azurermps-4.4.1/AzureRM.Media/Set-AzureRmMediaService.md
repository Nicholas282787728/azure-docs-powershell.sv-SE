---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 19db06ff5563e954124ab36274d62cce0e51b3a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581395"
---
# <span data-ttu-id="f2436-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="f2436-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="f2436-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2436-102">SYNOPSIS</span></span>
<span data-ttu-id="f2436-103">Ändrar angivna egenskaper för en befintlig medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="f2436-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2436-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2436-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tags <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2436-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2436-105">DESCRIPTION</span></span>
<span data-ttu-id="f2436-106">Cmdleten **set-AzureRmMediaService** ändrar angivna egenskaper för en befintlig medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="f2436-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="f2436-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2436-107">EXAMPLES</span></span>

### <span data-ttu-id="f2436-108">Exempel 1: ändra en befintlig medie tjänst</span><span class="sxs-lookup"><span data-stu-id="f2436-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="f2436-109">Det första kommandot skapar en serie Taggar och lagrar taggarna i variabeln som heter $Tags.</span><span class="sxs-lookup"><span data-stu-id="f2436-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="f2436-110">Det här andra kommandot uppdaterar medie tjänsten med namnet MediaService001 som tillhör resurs gruppen med namnet ResourceGroup123 med taggarna i $Tags variabel.</span><span class="sxs-lookup"><span data-stu-id="f2436-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="f2436-111">Kommandot använder också en matris med lagrings konfigurations objekt som lagras i $StorageAccounts variabel.</span><span class="sxs-lookup"><span data-stu-id="f2436-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="f2436-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2436-112">PARAMETERS</span></span>

### <span data-ttu-id="f2436-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2436-113">-AccountName</span></span>
<span data-ttu-id="f2436-114">Anger namnet på den medie tjänst som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="f2436-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f2436-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2436-115">-ResourceGroupName</span></span>
<span data-ttu-id="f2436-116">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f2436-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f2436-117">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f2436-117">-StorageAccounts</span></span>
<span data-ttu-id="f2436-118">Anger en matris med lagrings konton som denna cmdlet associerar med medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f2436-118">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="f2436-119">-Taggar</span><span class="sxs-lookup"><span data-stu-id="f2436-119">-Tags</span></span>
<span data-ttu-id="f2436-120">Anger taggar för medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f2436-120">Specifies tags for the media service.</span></span>

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

### <span data-ttu-id="f2436-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2436-121">-Confirm</span></span>
<span data-ttu-id="f2436-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2436-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2436-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2436-123">-WhatIf</span></span>
<span data-ttu-id="f2436-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2436-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2436-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2436-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2436-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2436-126">-DefaultProfile</span></span>
<span data-ttu-id="f2436-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2436-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2436-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2436-128">CommonParameters</span></span>
<span data-ttu-id="f2436-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2436-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2436-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2436-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2436-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2436-131">INPUTS</span></span>

## <span data-ttu-id="f2436-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2436-132">OUTPUTS</span></span>

### <span data-ttu-id="f2436-133">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="f2436-133">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="f2436-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2436-134">NOTES</span></span>

## <span data-ttu-id="f2436-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2436-135">RELATED LINKS</span></span>

[<span data-ttu-id="f2436-136">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="f2436-136">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="f2436-137">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="f2436-137">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="f2436-138">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="f2436-138">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


