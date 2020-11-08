---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099068"
---
# <span data-ttu-id="5318b-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5318b-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="5318b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5318b-102">SYNOPSIS</span></span>
<span data-ttu-id="5318b-103">Stoppar ett webb jobb för en webbplats.</span><span class="sxs-lookup"><span data-stu-id="5318b-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="5318b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5318b-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5318b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5318b-105">DESCRIPTION</span></span>
<span data-ttu-id="5318b-106">Cmdleten **Stop-AzureWebsiteJob** stoppar ett webb jobb för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5318b-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="5318b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5318b-107">EXAMPLES</span></span>

### <span data-ttu-id="5318b-108">Exempel 1: stoppa ett webb jobb för en webbplats</span><span class="sxs-lookup"><span data-stu-id="5318b-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="5318b-109">Stoppar ett webb jobb som heter MyWebJob för webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5318b-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="5318b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5318b-110">PARAMETERS</span></span>

### <span data-ttu-id="5318b-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="5318b-111">-JobName</span></span>
<span data-ttu-id="5318b-112">Namnet på webb jobbet.</span><span class="sxs-lookup"><span data-stu-id="5318b-112">The web job name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5318b-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="5318b-113">-Name</span></span>
<span data-ttu-id="5318b-114">Namnet på Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5318b-114">The name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5318b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5318b-115">-PassThru</span></span>
<span data-ttu-id="5318b-116">Returnerar ett booleskt värde som anger att jobbet har stoppats.</span><span class="sxs-lookup"><span data-stu-id="5318b-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="5318b-117">Denna cmdlet returnerar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5318b-117">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5318b-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="5318b-118">-Profile</span></span>
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

### <span data-ttu-id="5318b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="5318b-119">-Slot</span></span>
<span data-ttu-id="5318b-120">Plats namnet för Azure-webbplatsen.</span><span class="sxs-lookup"><span data-stu-id="5318b-120">The slot name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5318b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5318b-121">CommonParameters</span></span>
<span data-ttu-id="5318b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5318b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5318b-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5318b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5318b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5318b-124">INPUTS</span></span>

## <span data-ttu-id="5318b-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5318b-125">OUTPUTS</span></span>

## <span data-ttu-id="5318b-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5318b-126">NOTES</span></span>

## <span data-ttu-id="5318b-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5318b-127">RELATED LINKS</span></span>

[<span data-ttu-id="5318b-128">Stopp-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="5318b-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="5318b-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5318b-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="5318b-130">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5318b-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="5318b-131">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5318b-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="5318b-132">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="5318b-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


