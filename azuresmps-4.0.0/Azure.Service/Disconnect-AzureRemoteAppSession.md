---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093412"
---
# <span data-ttu-id="87eea-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="87eea-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="87eea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="87eea-102">SYNOPSIS</span></span>
<span data-ttu-id="87eea-103">Kopplar bort en Azure RemoteApp-session.</span><span class="sxs-lookup"><span data-stu-id="87eea-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="87eea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="87eea-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="87eea-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="87eea-105">DESCRIPTION</span></span>
<span data-ttu-id="87eea-106">Cmdleten **Koppla från-AzureRemoteAppSession** kopplas från en användares Azure RemoteApp-session.</span><span class="sxs-lookup"><span data-stu-id="87eea-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="87eea-107">Användarens klient kopplas från sin Azure RemoteApp-session, men användarnas program fortsätter att köras.</span><span class="sxs-lookup"><span data-stu-id="87eea-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="87eea-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="87eea-108">EXAMPLES</span></span>

### <span data-ttu-id="87eea-109">Exempel 1: koppla bort en användares session</span><span class="sxs-lookup"><span data-stu-id="87eea-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="87eea-110">Det här kommandot kopplar från Azure RemoteApp-sessionen i ContosoApps-samlingen för den användare vars UPN är PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="87eea-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="87eea-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="87eea-111">PARAMETERS</span></span>

### <span data-ttu-id="87eea-112">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="87eea-112">-CollectionName</span></span>
<span data-ttu-id="87eea-113">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="87eea-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="87eea-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="87eea-114">-Profile</span></span>
<span data-ttu-id="87eea-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="87eea-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87eea-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="87eea-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87eea-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="87eea-117">-UserUpn</span></span>
<span data-ttu-id="87eea-118">Anger användarens huvud namn (UPN) för en användare, till exempel PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="87eea-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="87eea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87eea-119">CommonParameters</span></span>
<span data-ttu-id="87eea-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87eea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87eea-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87eea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87eea-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="87eea-122">INPUTS</span></span>

## <span data-ttu-id="87eea-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="87eea-123">OUTPUTS</span></span>

## <span data-ttu-id="87eea-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="87eea-124">NOTES</span></span>

## <span data-ttu-id="87eea-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="87eea-125">RELATED LINKS</span></span>

[<span data-ttu-id="87eea-126">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="87eea-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="87eea-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="87eea-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="87eea-128">Skicka-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="87eea-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


