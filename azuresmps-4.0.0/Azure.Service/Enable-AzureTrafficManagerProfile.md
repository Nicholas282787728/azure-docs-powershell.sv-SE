---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099605"
---
# <span data-ttu-id="b2c70-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c70-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="b2c70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b2c70-102">SYNOPSIS</span></span>
<span data-ttu-id="b2c70-103">Aktiverar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="b2c70-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="b2c70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b2c70-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b2c70-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b2c70-105">DESCRIPTION</span></span>
<span data-ttu-id="b2c70-106">Cmdleten **Enable-AzureTrafficManagerProfile** aktiverar en Microsoft Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="b2c70-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b2c70-107">Ange parametern *Passthru* för att visa om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="b2c70-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="b2c70-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b2c70-108">EXAMPLES</span></span>

### <span data-ttu-id="b2c70-109">Exempel 1: Aktivera en Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="b2c70-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="b2c70-110">Det här kommandot aktiverar Traffic Manager-profilens profil.</span><span class="sxs-lookup"><span data-stu-id="b2c70-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="b2c70-111">Exempel 2: Aktivera en Traffic Manager-profil och visa resultatet</span><span class="sxs-lookup"><span data-stu-id="b2c70-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="b2c70-112">Det här kommandot aktiverar Traffic Manager-profilen med namnet min profil och visar om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="b2c70-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="b2c70-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b2c70-113">PARAMETERS</span></span>

### <span data-ttu-id="b2c70-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="b2c70-114">-Name</span></span>
<span data-ttu-id="b2c70-115">Anger namnet på Traffic Manager-profilen som ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="b2c70-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="b2c70-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b2c70-116">-PassThru</span></span>
<span data-ttu-id="b2c70-117">Returnerar $True om åtgärden lyckades. annars $False.</span><span class="sxs-lookup"><span data-stu-id="b2c70-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="b2c70-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="b2c70-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b2c70-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="b2c70-119">-Profile</span></span>
<span data-ttu-id="b2c70-120">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b2c70-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b2c70-121">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b2c70-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2c70-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2c70-122">CommonParameters</span></span>
<span data-ttu-id="b2c70-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2c70-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2c70-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2c70-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2c70-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b2c70-125">INPUTS</span></span>

## <span data-ttu-id="b2c70-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b2c70-126">OUTPUTS</span></span>

### <span data-ttu-id="b2c70-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b2c70-127">System.Boolean</span></span>
<span data-ttu-id="b2c70-128">Denna cmdlet skapar $True eller $False.</span><span class="sxs-lookup"><span data-stu-id="b2c70-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="b2c70-129">Om åtgärden lyckas och om du anger parametern *Passthru* returnerar denna cmdlet ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="b2c70-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="b2c70-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b2c70-130">NOTES</span></span>

## <span data-ttu-id="b2c70-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b2c70-131">RELATED LINKS</span></span>

[<span data-ttu-id="b2c70-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c70-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b2c70-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c70-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b2c70-134">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c70-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b2c70-135">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c70-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b2c70-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b2c70-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


