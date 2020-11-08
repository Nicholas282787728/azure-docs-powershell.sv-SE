---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A4E9C9A7-7FD2-4FD5-AB35-CFF717607B44
online version: ''
schema: 2.0.0
ms.openlocfilehash: c6da222e6cbfe02e181e4a863d8ce8d585215bdd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099377"
---
# <span data-ttu-id="e1b05-101">Remove-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="e1b05-101">Remove-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="e1b05-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1b05-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b05-103">Tar bort en användares användar disk från en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="e1b05-103">Removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e1b05-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1b05-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppUserDisk [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1b05-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1b05-105">DESCRIPTION</span></span>
<span data-ttu-id="e1b05-106">Cmdleten **Remove-AzureRemoteAppUserDisk** tar bort användarens disk från en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="e1b05-106">The **Remove-AzureRemoteAppUserDisk** cmdlet removes the user disk of a user from an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="e1b05-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1b05-107">EXAMPLES</span></span>

### <span data-ttu-id="e1b05-108">Exempel 1: ta bort en användar diskett</span><span class="sxs-lookup"><span data-stu-id="e1b05-108">Example 1: Remove a user disk</span></span>
```
PS C:\> Remove-AzureRemoteAppUserDisk -CollectionName "Contoso01" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="e1b05-109">Det här kommandot tar bort användar disken för en Azure Active Directory-användare som har UPN PattiFuller@contoso.com från samlingen Contoso01.</span><span class="sxs-lookup"><span data-stu-id="e1b05-109">This command removes the user disk of an Azure Active Directory user who has the UPN PattiFuller@contoso.com from the collection Contoso01.</span></span>

## <span data-ttu-id="e1b05-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1b05-110">PARAMETERS</span></span>

### <span data-ttu-id="e1b05-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="e1b05-111">-CollectionName</span></span>
<span data-ttu-id="e1b05-112">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="e1b05-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b05-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="e1b05-113">-Profile</span></span>
<span data-ttu-id="e1b05-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e1b05-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e1b05-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e1b05-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e1b05-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="e1b05-116">-UserUpn</span></span>
<span data-ttu-id="e1b05-117">Anger användarens huvud namn (UPN) för den användare som denna cmdlet tar bort disken för.</span><span class="sxs-lookup"><span data-stu-id="e1b05-117">Specifies the user principal name (UPN) of the user for whom this cmdlet removes the disk.</span></span>

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

### <span data-ttu-id="e1b05-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1b05-118">-Confirm</span></span>
<span data-ttu-id="e1b05-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1b05-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b05-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b05-120">-WhatIf</span></span>
<span data-ttu-id="e1b05-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1b05-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1b05-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1b05-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b05-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b05-123">CommonParameters</span></span>
<span data-ttu-id="e1b05-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1b05-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b05-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1b05-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b05-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1b05-126">INPUTS</span></span>

## <span data-ttu-id="e1b05-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1b05-127">OUTPUTS</span></span>

## <span data-ttu-id="e1b05-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1b05-128">NOTES</span></span>

## <span data-ttu-id="e1b05-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1b05-129">RELATED LINKS</span></span>

[<span data-ttu-id="e1b05-130">Copy-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="e1b05-130">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)


