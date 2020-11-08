---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261233"
---
# <span data-ttu-id="0cede-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0cede-101">Get-AzMediaService</span></span>

## <span data-ttu-id="0cede-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0cede-102">SYNOPSIS</span></span>
<span data-ttu-id="0cede-103">Hämtar information om en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="0cede-103">Gets information about a media service.</span></span>

## <span data-ttu-id="0cede-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0cede-104">SYNTAX</span></span>

### <span data-ttu-id="0cede-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cede-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0cede-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cede-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0cede-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0cede-107">DESCRIPTION</span></span>
<span data-ttu-id="0cede-108">Cmdleten **Get-AzMediaService** hämtar information om en medie tjänst.</span><span class="sxs-lookup"><span data-stu-id="0cede-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="0cede-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0cede-109">EXAMPLES</span></span>

### <span data-ttu-id="0cede-110">Exempel 1: Hämta alla medie tjänster i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="0cede-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="0cede-111">Det här kommandot får egenskaper för alla medie tjänster i resurs gruppen som heter ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="0cede-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="0cede-112">Exempel 2: Hämta egenskaper för medie tjänster</span><span class="sxs-lookup"><span data-stu-id="0cede-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="0cede-113">Det här kommandot får egenskaperna för medie tjänsten som heter MediaService1 som tillhör resurs gruppen med namnet ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="0cede-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="0cede-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0cede-114">PARAMETERS</span></span>

### <span data-ttu-id="0cede-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0cede-115">-AccountName</span></span>
<span data-ttu-id="0cede-116">Anger namnet på den medie tjänst som cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="0cede-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0cede-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cede-117">-DefaultProfile</span></span>
<span data-ttu-id="0cede-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0cede-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0cede-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cede-119">-ResourceGroupName</span></span>
<span data-ttu-id="0cede-120">Anger namnet på den resurs grupp som innehåller medie tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0cede-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="0cede-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cede-121">CommonParameters</span></span>
<span data-ttu-id="0cede-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cede-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cede-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cede-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cede-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0cede-124">INPUTS</span></span>

### <span data-ttu-id="0cede-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0cede-125">System.String</span></span>

## <span data-ttu-id="0cede-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0cede-126">OUTPUTS</span></span>

### <span data-ttu-id="0cede-127">Microsoft. Azure. commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="0cede-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="0cede-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0cede-128">NOTES</span></span>

## <span data-ttu-id="0cede-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0cede-129">RELATED LINKS</span></span>

[<span data-ttu-id="0cede-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0cede-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="0cede-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0cede-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="0cede-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0cede-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


