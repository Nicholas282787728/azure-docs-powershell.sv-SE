---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093463"
---
# <span data-ttu-id="4d83b-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4d83b-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="4d83b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d83b-102">SYNOPSIS</span></span>
<span data-ttu-id="4d83b-103">Uppdaterar en Azure RemoteApp-samling med en ny mall.</span><span class="sxs-lookup"><span data-stu-id="4d83b-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="4d83b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d83b-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d83b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d83b-105">DESCRIPTION</span></span>
<span data-ttu-id="4d83b-106">Cmdleten **Update-AzureRemoteAppCollection** uppdaterar en Azure RemoteApp-samling med en ny mall.</span><span class="sxs-lookup"><span data-stu-id="4d83b-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="4d83b-107">När uppdateringen är klar har användare med befintliga sessioner en timme för att logga ut innan de loggas ut automatiskt. När de loggar in igen ansluts de till den nyuppdaterade samlingen.</span><span class="sxs-lookup"><span data-stu-id="4d83b-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="4d83b-108">Om du vill att användarna ska loggas ut omedelbart när samlingen uppdateras anger du parametern *ForceLogoffWhenUpdateComplete* .</span><span class="sxs-lookup"><span data-stu-id="4d83b-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="4d83b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d83b-109">EXAMPLES</span></span>

## <span data-ttu-id="4d83b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d83b-110">PARAMETERS</span></span>

### <span data-ttu-id="4d83b-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="4d83b-111">-CollectionName</span></span>
<span data-ttu-id="4d83b-112">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="4d83b-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d83b-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="4d83b-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="4d83b-114">Anger att denna cmdlet signerar användarna från sina befintliga sessioner så fort uppdateringen är klar.</span><span class="sxs-lookup"><span data-stu-id="4d83b-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="4d83b-115">När användarna loggar in igen ansluter de till den nyuppdaterade samlingen.</span><span class="sxs-lookup"><span data-stu-id="4d83b-115">When users sign in again, they connect to the newly updated collection.</span></span>

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

### <span data-ttu-id="4d83b-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="4d83b-116">-ImageName</span></span>
<span data-ttu-id="4d83b-117">Anger namnet på en Azure RemoteApp-mallfil.</span><span class="sxs-lookup"><span data-stu-id="4d83b-117">Specifies the name of an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d83b-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="4d83b-118">-Profile</span></span>
<span data-ttu-id="4d83b-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="4d83b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4d83b-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="4d83b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4d83b-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4d83b-121">-SubnetName</span></span>
<span data-ttu-id="4d83b-122">Anger namnet på det undernät som samlingen ska flyttas till.</span><span class="sxs-lookup"><span data-stu-id="4d83b-122">Specifies the name of the subnet into which to move the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d83b-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d83b-123">-Confirm</span></span>
<span data-ttu-id="4d83b-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d83b-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d83b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d83b-125">-WhatIf</span></span>
<span data-ttu-id="4d83b-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d83b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d83b-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d83b-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d83b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d83b-128">CommonParameters</span></span>
<span data-ttu-id="4d83b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d83b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d83b-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d83b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d83b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d83b-131">INPUTS</span></span>

## <span data-ttu-id="4d83b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d83b-132">OUTPUTS</span></span>

## <span data-ttu-id="4d83b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d83b-133">NOTES</span></span>

## <span data-ttu-id="4d83b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d83b-134">RELATED LINKS</span></span>

[<span data-ttu-id="4d83b-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4d83b-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="4d83b-136">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4d83b-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="4d83b-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="4d83b-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


