---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9ddf8291d5f6276126cea82305bbc554d05ca006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584164"
---
# <span data-ttu-id="8f98d-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8f98d-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="8f98d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f98d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f98d-103">Tar bort en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="8f98d-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f98d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f98d-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f98d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f98d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f98d-106">Cmdleten **Remove-AzureRmMediaService** tar bort en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="8f98d-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="8f98d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f98d-107">EXAMPLES</span></span>

### <span data-ttu-id="8f98d-108">Exempel 1: ta bort en medie tjänst</span><span class="sxs-lookup"><span data-stu-id="8f98d-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="8f98d-109">Det här kommandot tar bort medie tjänsten med namnet MediaService0011 i resurs gruppen som heter ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="8f98d-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="8f98d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f98d-110">PARAMETERS</span></span>

### <span data-ttu-id="8f98d-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8f98d-111">-AccountName</span></span>
<span data-ttu-id="8f98d-112">Anger namnet på den medie tjänst som cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="8f98d-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8f98d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f98d-113">-DefaultProfile</span></span>
<span data-ttu-id="8f98d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8f98d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f98d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8f98d-115">-Force</span></span>
<span data-ttu-id="8f98d-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8f98d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f98d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f98d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f98d-118">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8f98d-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="8f98d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f98d-119">-Confirm</span></span>
<span data-ttu-id="8f98d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f98d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f98d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f98d-121">-WhatIf</span></span>
<span data-ttu-id="8f98d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f98d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f98d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f98d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f98d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f98d-124">CommonParameters</span></span>
<span data-ttu-id="8f98d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f98d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f98d-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f98d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f98d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f98d-127">INPUTS</span></span>

### <span data-ttu-id="8f98d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8f98d-128">System.String</span></span>

## <span data-ttu-id="8f98d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f98d-129">OUTPUTS</span></span>

### <span data-ttu-id="8f98d-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8f98d-130">System.Boolean</span></span>

## <span data-ttu-id="8f98d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f98d-131">NOTES</span></span>

## <span data-ttu-id="8f98d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f98d-132">RELATED LINKS</span></span>

[<span data-ttu-id="8f98d-133">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8f98d-133">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="8f98d-134">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8f98d-134">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="8f98d-135">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="8f98d-135">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


