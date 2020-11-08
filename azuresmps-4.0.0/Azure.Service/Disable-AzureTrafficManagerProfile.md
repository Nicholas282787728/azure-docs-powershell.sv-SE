---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093419"
---
# <span data-ttu-id="2d2ce-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2d2ce-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="2d2ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2ce-103">Inaktiverar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="2d2ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d2ce-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2d2ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="2d2ce-106">Cmdleten **disable-AzureTrafficManagerProfile** inaktiverar en Microsoft Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="2d2ce-107">Du kan använda parametern *Passthru* för att visa om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="2d2ce-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d2ce-108">EXAMPLES</span></span>

### <span data-ttu-id="2d2ce-109">Exempel 1: inaktivera en Traffic Manager-profil och visa resultatet</span><span class="sxs-lookup"><span data-stu-id="2d2ce-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="2d2ce-110">Det här kommandot inaktiverar Traffic Manager-profilen med namnet min-profil.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="2d2ce-111">Kommandot anger parametern *Passthru* för att visa om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="2d2ce-112">Exempel 2: inaktivera en Traffic Manager-profil och Visa inga resultat</span><span class="sxs-lookup"><span data-stu-id="2d2ce-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="2d2ce-113">Det här kommandot inaktiverar Traffic Manager-profilen med namnet min profil men visar inte om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="2d2ce-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d2ce-114">PARAMETERS</span></span>

### <span data-ttu-id="2d2ce-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d2ce-115">-Name</span></span>
<span data-ttu-id="2d2ce-116">Anger namnet på Traffic Manager-profilen som ska avaktiveras.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="2d2ce-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d2ce-117">-PassThru</span></span>
<span data-ttu-id="2d2ce-118">Returnerar $True om åtgärden lyckades. annars $False.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="2d2ce-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2d2ce-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="2d2ce-120">-Profile</span></span>
<span data-ttu-id="2d2ce-121">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2d2ce-122">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2d2ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2ce-123">CommonParameters</span></span>
<span data-ttu-id="2d2ce-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2ce-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d2ce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2ce-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d2ce-126">INPUTS</span></span>

## <span data-ttu-id="2d2ce-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d2ce-127">OUTPUTS</span></span>

### <span data-ttu-id="2d2ce-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d2ce-128">System.Boolean</span></span>
<span data-ttu-id="2d2ce-129">Denna cmdlet skapar $True eller $False.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="2d2ce-130">Om åtgärden lyckas och om du anger parametern *Passthru* returnerar denna cmdlet ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="2d2ce-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="2d2ce-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d2ce-131">NOTES</span></span>

## <span data-ttu-id="2d2ce-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d2ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="2d2ce-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2d2ce-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2d2ce-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2d2ce-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2d2ce-135">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2d2ce-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2d2ce-136">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2d2ce-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="2d2ce-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2d2ce-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


