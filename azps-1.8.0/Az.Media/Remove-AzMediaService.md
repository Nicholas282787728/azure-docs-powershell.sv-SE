---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: f9d0ee722f828aba251c9776c231338b54c0580c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93915757"
---
# <span data-ttu-id="1e1d1-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e1d1-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="1e1d1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1d1-103">Tar bort en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-103">Removes a media service.</span></span>

## <span data-ttu-id="1e1d1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e1d1-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e1d1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e1d1-105">DESCRIPTION</span></span>
<span data-ttu-id="1e1d1-106">Cmdleten **Remove-AzMediaService** tar bort en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="1e1d1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e1d1-107">EXAMPLES</span></span>

### <span data-ttu-id="1e1d1-108">Exempel 1: ta bort en medie tjänst</span><span class="sxs-lookup"><span data-stu-id="1e1d1-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="1e1d1-109">Det här kommandot tar bort medie tjänsten med namnet MediaService0011 i resurs gruppen som heter ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="1e1d1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e1d1-110">PARAMETERS</span></span>

### <span data-ttu-id="1e1d1-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1e1d1-111">-AccountName</span></span>
<span data-ttu-id="1e1d1-112">Anger namnet på den medie tjänst som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1e1d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e1d1-113">-DefaultProfile</span></span>
<span data-ttu-id="1e1d1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1e1d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e1d1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1e1d1-115">-Force</span></span>
<span data-ttu-id="1e1d1-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e1d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e1d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e1d1-118">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="1e1d1-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e1d1-119">-Confirm</span></span>
<span data-ttu-id="1e1d1-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e1d1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e1d1-121">-WhatIf</span></span>
<span data-ttu-id="1e1d1-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e1d1-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e1d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1d1-124">CommonParameters</span></span>
<span data-ttu-id="1e1d1-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e1d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1d1-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e1d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1d1-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e1d1-127">INPUTS</span></span>

### <span data-ttu-id="1e1d1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1e1d1-128">System.String</span></span>

## <span data-ttu-id="1e1d1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e1d1-129">OUTPUTS</span></span>

### <span data-ttu-id="1e1d1-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e1d1-130">System.Boolean</span></span>

## <span data-ttu-id="1e1d1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e1d1-131">NOTES</span></span>

## <span data-ttu-id="1e1d1-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e1d1-132">RELATED LINKS</span></span>

[<span data-ttu-id="1e1d1-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e1d1-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="1e1d1-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e1d1-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="1e1d1-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e1d1-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


