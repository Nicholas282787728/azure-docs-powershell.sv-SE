---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 29602F63-A05B-45AF-8DD8-5EBBF4C33FCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32af8d2e89c14b0d36265efc688a88858851bba5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099402"
---
# <span data-ttu-id="05e7c-101">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="05e7c-101">Remove-AzureAffinityGroup</span></span>

## <span data-ttu-id="05e7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="05e7c-103">Tar bort en tillhörighets grupp i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="05e7c-103">Deletes an affinity group in a subscription.</span></span>

## <span data-ttu-id="05e7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05e7c-104">SYNTAX</span></span>

```
Remove-AzureAffinityGroup [-Name] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="05e7c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="05e7c-106">Cmdleten **Remove-AzureAffinityGroup** tar bort en Azure tillhörighets grupp i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="05e7c-106">The **Remove-AzureAffinityGroup** cmdlet deletes an Azure affinity group in the current subscription.</span></span>
<span data-ttu-id="05e7c-107">Du kan inte ta bort en tillhörighets grupp som har medlemmar.</span><span class="sxs-lookup"><span data-stu-id="05e7c-107">You cannot delete an affinity group that has any members.</span></span>
<span data-ttu-id="05e7c-108">Du måste först ta bort alla medlemmar i en tillhörighets grupp.</span><span class="sxs-lookup"><span data-stu-id="05e7c-108">You must first delete all the members of an affinity group.</span></span>

## <span data-ttu-id="05e7c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05e7c-109">EXAMPLES</span></span>

### <span data-ttu-id="05e7c-110">Exempel 1: ta bort en tillhörighets grupp</span><span class="sxs-lookup"><span data-stu-id="05e7c-110">Example 1: Remove an affinity group</span></span>
```
PS C:\> Remove-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="05e7c-111">Det här kommandot tar bort South01-tillhörighets gruppen i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="05e7c-111">This command deletes the South01 affinity group in the current subscription.</span></span>

## <span data-ttu-id="05e7c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05e7c-112">PARAMETERS</span></span>

### <span data-ttu-id="05e7c-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="05e7c-113">-InformationAction</span></span>
<span data-ttu-id="05e7c-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="05e7c-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="05e7c-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="05e7c-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="05e7c-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="05e7c-116">Continue</span></span>
- <span data-ttu-id="05e7c-117">Över</span><span class="sxs-lookup"><span data-stu-id="05e7c-117">Ignore</span></span>
- <span data-ttu-id="05e7c-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="05e7c-118">Inquire</span></span>
- <span data-ttu-id="05e7c-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="05e7c-119">SilentlyContinue</span></span>
- <span data-ttu-id="05e7c-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="05e7c-120">Stop</span></span>
- <span data-ttu-id="05e7c-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="05e7c-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e7c-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="05e7c-122">-InformationVariable</span></span>
<span data-ttu-id="05e7c-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="05e7c-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e7c-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="05e7c-124">-Name</span></span>
<span data-ttu-id="05e7c-125">Anger namnet på den tillhörighets grupp som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="05e7c-125">Specifies the name of the affinity group that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05e7c-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="05e7c-126">-Profile</span></span>
<span data-ttu-id="05e7c-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="05e7c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05e7c-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="05e7c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05e7c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e7c-129">CommonParameters</span></span>
<span data-ttu-id="05e7c-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e7c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e7c-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e7c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e7c-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05e7c-132">INPUTS</span></span>

## <span data-ttu-id="05e7c-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05e7c-133">OUTPUTS</span></span>

## <span data-ttu-id="05e7c-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05e7c-134">NOTES</span></span>

## <span data-ttu-id="05e7c-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05e7c-135">RELATED LINKS</span></span>

[<span data-ttu-id="05e7c-136">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="05e7c-136">Get-AzureAffinityGroup</span></span>](./Get-AzureAffinityGroup.md)

[<span data-ttu-id="05e7c-137">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="05e7c-137">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="05e7c-138">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="05e7c-138">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


