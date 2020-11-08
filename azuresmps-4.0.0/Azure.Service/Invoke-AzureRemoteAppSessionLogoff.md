---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 87163619-DEA4-4183-BB11-2D7B16F4BE8A
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee4e094c1e38c54b1f9ad4e78723ec49fff1f75b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099477"
---
# <span data-ttu-id="22d64-101">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="22d64-101">Invoke-AzureRemoteAppSessionLogoff</span></span>

## <span data-ttu-id="22d64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22d64-102">SYNOPSIS</span></span>
<span data-ttu-id="22d64-103">Loggar ut direkt från en Azure RemoteApp-session.</span><span class="sxs-lookup"><span data-stu-id="22d64-103">Logs off an Azure RemoteApp session immediately.</span></span>

## <span data-ttu-id="22d64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22d64-104">SYNTAX</span></span>

```
Invoke-AzureRemoteAppSessionLogoff [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22d64-105">DESCRIPTION</span></span>
<span data-ttu-id="22d64-106">Cmdleten **Invoke-AzureRemoteAppSessionLogoff** loggar omedelbart ut en användare från en fjärrsession som körs i Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="22d64-106">The **Invoke-AzureRemoteAppSessionLogoff** cmdlet immediately logs off a user from a remote session running in Azure RemoteApp.</span></span>

## <span data-ttu-id="22d64-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22d64-107">EXAMPLES</span></span>

### <span data-ttu-id="22d64-108">Exempel 1: Logga ut en användare</span><span class="sxs-lookup"><span data-stu-id="22d64-108">Example 1: Log off a user</span></span>
```
PS C:\> Invoke-AzureRemoteAppSessionLogoff -CollectionName ContosoApps -UserUpn PattiFuller@contoso.com
```

<span data-ttu-id="22d64-109">Det här kommandot loggar ut den användare vars UPN är PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="22d64-109">This command logs off the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="22d64-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22d64-110">PARAMETERS</span></span>

### <span data-ttu-id="22d64-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="22d64-111">-CollectionName</span></span>
<span data-ttu-id="22d64-112">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="22d64-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="22d64-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="22d64-113">-Profile</span></span>
<span data-ttu-id="22d64-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="22d64-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22d64-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="22d64-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="22d64-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="22d64-116">-UserUpn</span></span>
<span data-ttu-id="22d64-117">Specifes användarens huvud namn (UPN) för en användare, till exempel PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="22d64-117">Specifes the user Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="22d64-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22d64-118">-Confirm</span></span>
<span data-ttu-id="22d64-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22d64-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d64-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d64-120">-WhatIf</span></span>
<span data-ttu-id="22d64-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22d64-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d64-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22d64-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d64-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d64-123">CommonParameters</span></span>
<span data-ttu-id="22d64-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d64-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d64-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d64-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d64-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22d64-126">INPUTS</span></span>

## <span data-ttu-id="22d64-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22d64-127">OUTPUTS</span></span>

## <span data-ttu-id="22d64-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22d64-128">NOTES</span></span>

## <span data-ttu-id="22d64-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22d64-129">RELATED LINKS</span></span>

[<span data-ttu-id="22d64-130">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="22d64-130">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="22d64-131">Koppla från-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="22d64-131">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="22d64-132">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="22d64-132">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)


