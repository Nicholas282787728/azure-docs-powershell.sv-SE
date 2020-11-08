---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099321"
---
# <span data-ttu-id="a5111-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5111-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="a5111-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5111-102">SYNOPSIS</span></span>
<span data-ttu-id="a5111-103">Tar bort en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="a5111-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="a5111-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5111-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5111-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5111-105">DESCRIPTION</span></span>
<span data-ttu-id="a5111-106">Cmdleten **Remove-AzureTrafficManagerProfile** tar bort en Microsoft Azure Traffic Manager-profil från den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a5111-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="a5111-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5111-107">EXAMPLES</span></span>

### <span data-ttu-id="a5111-108">Exempel 1: ta bort en Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="a5111-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="a5111-109">Det här kommandot tar bort Traffic Manager-profilens profil.</span><span class="sxs-lookup"><span data-stu-id="a5111-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="a5111-110">Exempel 2: ta bort en Traffic Manager-profil</span><span class="sxs-lookup"><span data-stu-id="a5111-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="a5111-111">Det här kommandot tar bort Traffic Manager-profilen med namnet min profil utan att fråga dig om bekräftelse och returnerar resultaten.</span><span class="sxs-lookup"><span data-stu-id="a5111-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="a5111-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5111-112">PARAMETERS</span></span>

### <span data-ttu-id="a5111-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a5111-113">-Force</span></span>
<span data-ttu-id="a5111-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a5111-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5111-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5111-115">-Name</span></span>
<span data-ttu-id="a5111-116">Anger namnet på den Traffic Manager-profil som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a5111-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="a5111-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5111-117">-PassThru</span></span>
<span data-ttu-id="a5111-118">Returnerar $True om åtgärden lyckades. annars $False.</span><span class="sxs-lookup"><span data-stu-id="a5111-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="a5111-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a5111-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5111-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="a5111-120">-Profile</span></span>
<span data-ttu-id="a5111-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="a5111-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a5111-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="a5111-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a5111-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5111-123">CommonParameters</span></span>
<span data-ttu-id="a5111-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5111-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5111-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5111-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5111-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5111-126">INPUTS</span></span>

## <span data-ttu-id="a5111-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5111-127">OUTPUTS</span></span>

### <span data-ttu-id="a5111-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5111-128">System.Boolean</span></span>
<span data-ttu-id="a5111-129">Denna cmdlet skapar $True eller $False.</span><span class="sxs-lookup"><span data-stu-id="a5111-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="a5111-130">Om åtgärden lyckas och om du anger parametern *Passthru* returnerar denna cmdlet ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="a5111-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="a5111-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5111-131">NOTES</span></span>

## <span data-ttu-id="a5111-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5111-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5111-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5111-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="a5111-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5111-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="a5111-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5111-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="a5111-136">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5111-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="a5111-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a5111-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


