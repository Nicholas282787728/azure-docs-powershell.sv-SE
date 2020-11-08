---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093200"
---
# <span data-ttu-id="44d81-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="44d81-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="44d81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44d81-102">SYNOPSIS</span></span>
<span data-ttu-id="44d81-103">Byter namn på en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="44d81-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="44d81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44d81-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="44d81-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44d81-105">DESCRIPTION</span></span>
<span data-ttu-id="44d81-106">Cmdleten **rename-AzureRemoteAppTemplateImage** byter namn på en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="44d81-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="44d81-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44d81-107">EXAMPLES</span></span>

### <span data-ttu-id="44d81-108">Exempel 1: Byt namn på en mall</span><span class="sxs-lookup"><span data-stu-id="44d81-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="44d81-109">Det här kommandot byter namn på Azure RemoteApp-mallen med namnet ContosoApps till ContosoFinanceApps.</span><span class="sxs-lookup"><span data-stu-id="44d81-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="44d81-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44d81-110">PARAMETERS</span></span>

### <span data-ttu-id="44d81-111">-ImageName</span><span class="sxs-lookup"><span data-stu-id="44d81-111">-ImageName</span></span>
<span data-ttu-id="44d81-112">Anger namnet på en Azure RemoteApp-mallfil för att byta namn.</span><span class="sxs-lookup"><span data-stu-id="44d81-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

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

### <span data-ttu-id="44d81-113">-NewName</span><span class="sxs-lookup"><span data-stu-id="44d81-113">-NewName</span></span>
<span data-ttu-id="44d81-114">Anger ett nytt namn på en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="44d81-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d81-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="44d81-115">-Profile</span></span>
<span data-ttu-id="44d81-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="44d81-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="44d81-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="44d81-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="44d81-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d81-118">CommonParameters</span></span>
<span data-ttu-id="44d81-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d81-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d81-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d81-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d81-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44d81-121">INPUTS</span></span>

## <span data-ttu-id="44d81-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44d81-122">OUTPUTS</span></span>

## <span data-ttu-id="44d81-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44d81-123">NOTES</span></span>

## <span data-ttu-id="44d81-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44d81-124">RELATED LINKS</span></span>

[<span data-ttu-id="44d81-125">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="44d81-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="44d81-126">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="44d81-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="44d81-127">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="44d81-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)


