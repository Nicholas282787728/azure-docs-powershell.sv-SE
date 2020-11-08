---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DAEA68EF-8153-4E03-B539-B720EA14776C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6e2040b648b162386a9caf73f701a09413bb20d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099809"
---
# <span data-ttu-id="1459c-101">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="1459c-101">Get-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="1459c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1459c-102">SYNOPSIS</span></span>
<span data-ttu-id="1459c-103">Hämtar information om Azure RemoteApp-mallfiler.</span><span class="sxs-lookup"><span data-stu-id="1459c-103">Retrieves information about Azure RemoteApp template images.</span></span>

## <span data-ttu-id="1459c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1459c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppTemplateImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1459c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1459c-105">DESCRIPTION</span></span>
<span data-ttu-id="1459c-106">Cmdleten **Get-AzureRemoteAppTemplateImage** hämtar information om Azure RemoteApp-mallfiler i Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1459c-106">The **Get-AzureRemoteAppTemplateImage** cmdlet retrieves information about Azure RemoteApp template images in Microsoft Azure.</span></span>
<span data-ttu-id="1459c-107">Denna cmdlet returnerar ett objekt som innehåller information om en viss Malltyp.</span><span class="sxs-lookup"><span data-stu-id="1459c-107">This cmdlet returns an object containing information about a specified template image.</span></span>
<span data-ttu-id="1459c-108">Om ingen Malltyp anges hämtar den information om alla mallfiler i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="1459c-108">If no template image is specified, it retrieves information about all the template images in the current subscription.</span></span>

## <span data-ttu-id="1459c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1459c-109">EXAMPLES</span></span>

### <span data-ttu-id="1459c-110">Exempel 1: få en lista över alla listmallar</span><span class="sxs-lookup"><span data-stu-id="1459c-110">Example 1: Get a list of all template images</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage
```

<span data-ttu-id="1459c-111">Det här kommandot returnerar listan över alla listmallar.</span><span class="sxs-lookup"><span data-stu-id="1459c-111">This command returns the list of all template images.</span></span>

### <span data-ttu-id="1459c-112">Exempel 2: Hämta information om en viss Malltyp</span><span class="sxs-lookup"><span data-stu-id="1459c-112">Example 2: Retrieve information about a specified template image</span></span>
```
PS C:\> Get-AzureRemoteAppTemplateImage -ImageName "ContosoApps"
```

<span data-ttu-id="1459c-113">Det här kommandot hämtar information om den mallfiler som heter ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="1459c-113">This command retrieves information about the template image named ContosoApps.</span></span>

## <span data-ttu-id="1459c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1459c-114">PARAMETERS</span></span>

### <span data-ttu-id="1459c-115">-ImageName</span><span class="sxs-lookup"><span data-stu-id="1459c-115">-ImageName</span></span>
<span data-ttu-id="1459c-116">Anger namnet på en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="1459c-116">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="1459c-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="1459c-117">-Profile</span></span>
<span data-ttu-id="1459c-118">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="1459c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1459c-119">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="1459c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1459c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1459c-120">CommonParameters</span></span>
<span data-ttu-id="1459c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1459c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1459c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1459c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1459c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1459c-123">INPUTS</span></span>

## <span data-ttu-id="1459c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1459c-124">OUTPUTS</span></span>

## <span data-ttu-id="1459c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1459c-125">NOTES</span></span>

## <span data-ttu-id="1459c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1459c-126">RELATED LINKS</span></span>

[<span data-ttu-id="1459c-127">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="1459c-127">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="1459c-128">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="1459c-128">Get-AzureRemoteAppStartMenuProgram</span></span>](./Get-AzureRemoteAppStartMenuProgram.md)


