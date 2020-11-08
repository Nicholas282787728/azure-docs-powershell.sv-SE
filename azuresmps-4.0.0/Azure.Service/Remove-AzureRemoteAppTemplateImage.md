---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B35979E5-94C4-4DCC-B87D-D6915464CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91d464abcd8b67a0fff2cd897fa6f45fe6cb3d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099379"
---
# <span data-ttu-id="074ef-101">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="074ef-101">Remove-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="074ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="074ef-102">SYNOPSIS</span></span>
<span data-ttu-id="074ef-103">Tar bort en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="074ef-103">Deletes an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="074ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="074ef-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppTemplateImage [-ImageName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="074ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="074ef-105">DESCRIPTION</span></span>
<span data-ttu-id="074ef-106">Cmdleten **Remove-AzureRemoteAppTemplateImage** tar bort en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="074ef-106">The **Remove-AzureRemoteAppTemplateImage** cmdlet deletes an Azure RemoteApp template image.</span></span>
<span data-ttu-id="074ef-107">En mall kan bara tas bort om den inte är länkad till någon Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="074ef-107">A template image can deleted only if it is not linked to any Azure RemoteApp collection.</span></span>

## <span data-ttu-id="074ef-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="074ef-108">EXAMPLES</span></span>

### <span data-ttu-id="074ef-109">Exempel 1: ta bort en mall</span><span class="sxs-lookup"><span data-stu-id="074ef-109">Example 1: Delete a template image</span></span>
```
PS C:\> Remove-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="074ef-110">Det här kommandot tar bort den mallfiler som heter ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="074ef-110">This command deletes the template image named ContosoApps.</span></span>

## <span data-ttu-id="074ef-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="074ef-111">PARAMETERS</span></span>

### <span data-ttu-id="074ef-112">-ImageName</span><span class="sxs-lookup"><span data-stu-id="074ef-112">-ImageName</span></span>
<span data-ttu-id="074ef-113">Anger namnet på RemoteApp-mallen.</span><span class="sxs-lookup"><span data-stu-id="074ef-113">Specifies the name of the RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="074ef-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="074ef-114">-Profile</span></span>
<span data-ttu-id="074ef-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="074ef-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="074ef-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="074ef-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="074ef-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="074ef-117">-Confirm</span></span>
<span data-ttu-id="074ef-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="074ef-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="074ef-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="074ef-119">-WhatIf</span></span>
<span data-ttu-id="074ef-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="074ef-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="074ef-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="074ef-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="074ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="074ef-122">CommonParameters</span></span>
<span data-ttu-id="074ef-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="074ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="074ef-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="074ef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="074ef-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="074ef-125">INPUTS</span></span>

## <span data-ttu-id="074ef-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="074ef-126">OUTPUTS</span></span>

## <span data-ttu-id="074ef-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="074ef-127">NOTES</span></span>

## <span data-ttu-id="074ef-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="074ef-128">RELATED LINKS</span></span>

[<span data-ttu-id="074ef-129">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="074ef-129">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="074ef-130">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="074ef-130">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="074ef-131">Rename – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="074ef-131">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


