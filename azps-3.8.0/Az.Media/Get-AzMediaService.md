---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092261"
---
# <span data-ttu-id="623eb-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="623eb-101">Get-AzMediaService</span></span>

## <span data-ttu-id="623eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="623eb-102">SYNOPSIS</span></span>
<span data-ttu-id="623eb-103">Hämtar information om en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="623eb-103">Gets information about a media service.</span></span>

## <span data-ttu-id="623eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="623eb-104">SYNTAX</span></span>

### <span data-ttu-id="623eb-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="623eb-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="623eb-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="623eb-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="623eb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="623eb-107">DESCRIPTION</span></span>
<span data-ttu-id="623eb-108">Cmdleten **Get-AzMediaService** hämtar information om en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="623eb-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="623eb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="623eb-109">EXAMPLES</span></span>

### <span data-ttu-id="623eb-110">Exempel 1: Hämta alla medie tjänster i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="623eb-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="623eb-111">Det här kommandot får egenskaper för alla medie tjänster i resurs gruppen som heter ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="623eb-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="623eb-112">Exempel 2: Hämta egenskaper för medie tjänster</span><span class="sxs-lookup"><span data-stu-id="623eb-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="623eb-113">Det här kommandot får egenskaperna för medie tjänsten som heter MediaService1 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="623eb-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="623eb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="623eb-114">PARAMETERS</span></span>

### <span data-ttu-id="623eb-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="623eb-115">-AccountName</span></span>
<span data-ttu-id="623eb-116">Anger namnet på den medie tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="623eb-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="623eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="623eb-117">-DefaultProfile</span></span>
<span data-ttu-id="623eb-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="623eb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="623eb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="623eb-119">-ResourceGroupName</span></span>
<span data-ttu-id="623eb-120">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="623eb-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="623eb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="623eb-121">CommonParameters</span></span>
<span data-ttu-id="623eb-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="623eb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="623eb-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="623eb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="623eb-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="623eb-124">INPUTS</span></span>

### <span data-ttu-id="623eb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="623eb-125">System.String</span></span>

## <span data-ttu-id="623eb-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="623eb-126">OUTPUTS</span></span>

### <span data-ttu-id="623eb-127">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="623eb-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="623eb-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="623eb-128">NOTES</span></span>

## <span data-ttu-id="623eb-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="623eb-129">RELATED LINKS</span></span>

[<span data-ttu-id="623eb-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="623eb-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="623eb-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="623eb-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="623eb-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="623eb-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


