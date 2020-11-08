---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099807"
---
# <span data-ttu-id="5d646-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="5d646-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="5d646-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d646-102">SYNOPSIS</span></span>
<span data-ttu-id="5d646-103">Visar en lista över alla aktiva och frånkopplade Azure RemoteApp-sessioner för en samling.</span><span class="sxs-lookup"><span data-stu-id="5d646-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="5d646-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d646-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d646-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d646-105">DESCRIPTION</span></span>
<span data-ttu-id="5d646-106">Cmdleten **Get-AzureRemoteAppSession** visar alla aktiva och frånkopplade Azure RemoteApp-sessioner för en Azure RemoteApp-samling.</span><span class="sxs-lookup"><span data-stu-id="5d646-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5d646-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d646-107">EXAMPLES</span></span>

### <span data-ttu-id="5d646-108">Exempel 1: lista alla sessioner i en samling</span><span class="sxs-lookup"><span data-stu-id="5d646-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="5d646-109">Det här kommandot visar alla sessioner i Azure RemoteApp-samlingen med namnet ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="5d646-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="5d646-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d646-110">PARAMETERS</span></span>

### <span data-ttu-id="5d646-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="5d646-111">-CollectionName</span></span>
<span data-ttu-id="5d646-112">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="5d646-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="5d646-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="5d646-113">-Profile</span></span>
<span data-ttu-id="5d646-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="5d646-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5d646-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="5d646-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5d646-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="5d646-116">-UserUpn</span></span>
<span data-ttu-id="5d646-117">Anger användarens huvud namn (UPN) för en användare som ska få Azure RemoteApp-sessioner.</span><span class="sxs-lookup"><span data-stu-id="5d646-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="5d646-118">UPN kan till exempel vara i följande format: PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="5d646-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="5d646-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d646-119">CommonParameters</span></span>
<span data-ttu-id="5d646-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d646-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d646-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d646-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d646-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d646-122">INPUTS</span></span>

## <span data-ttu-id="5d646-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d646-123">OUTPUTS</span></span>

## <span data-ttu-id="5d646-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d646-124">NOTES</span></span>

## <span data-ttu-id="5d646-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d646-125">RELATED LINKS</span></span>

[<span data-ttu-id="5d646-126">Koppla från-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="5d646-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="5d646-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="5d646-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="5d646-128">Skicka-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="5d646-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


