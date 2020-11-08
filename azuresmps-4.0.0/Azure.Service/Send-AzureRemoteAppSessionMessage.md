---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099663"
---
# <span data-ttu-id="7b38c-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="7b38c-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="7b38c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b38c-102">SYNOPSIS</span></span>
<span data-ttu-id="7b38c-103">Skickar ett meddelande till en användare.</span><span class="sxs-lookup"><span data-stu-id="7b38c-103">Sends a message to a user.</span></span>

## <span data-ttu-id="7b38c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b38c-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7b38c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b38c-105">DESCRIPTION</span></span>
<span data-ttu-id="7b38c-106">Cmdleten **send-AzureRemoteAppSessionMessage** skickar ett meddelande till en användare som är ansluten till en Azure RemoteApp-session.</span><span class="sxs-lookup"><span data-stu-id="7b38c-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="7b38c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b38c-107">EXAMPLES</span></span>

### <span data-ttu-id="7b38c-108">Exempel 1: Skicka ett meddelande till en användare</span><span class="sxs-lookup"><span data-stu-id="7b38c-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="7b38c-109">Det här kommandot skickar ett meddelande till den användare vars UPN är PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="7b38c-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="7b38c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b38c-110">PARAMETERS</span></span>

### <span data-ttu-id="7b38c-111">-Samlings namn</span><span class="sxs-lookup"><span data-stu-id="7b38c-111">-CollectionName</span></span>
<span data-ttu-id="7b38c-112">Anger namnet på Azure RemoteApp-samlingen.</span><span class="sxs-lookup"><span data-stu-id="7b38c-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="7b38c-113">– Meddelande</span><span class="sxs-lookup"><span data-stu-id="7b38c-113">-Message</span></span>
<span data-ttu-id="7b38c-114">Anger det meddelande som ska skickas.</span><span class="sxs-lookup"><span data-stu-id="7b38c-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b38c-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="7b38c-115">-Profile</span></span>
<span data-ttu-id="7b38c-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="7b38c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7b38c-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="7b38c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7b38c-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="7b38c-118">-UserUpn</span></span>
<span data-ttu-id="7b38c-119">Anger användarens huvud namn (UPN) för en användare, till exempel PattiFuller@contoso.com .</span><span class="sxs-lookup"><span data-stu-id="7b38c-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="7b38c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b38c-120">CommonParameters</span></span>
<span data-ttu-id="7b38c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b38c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b38c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b38c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b38c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b38c-123">INPUTS</span></span>

## <span data-ttu-id="7b38c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b38c-124">OUTPUTS</span></span>

## <span data-ttu-id="7b38c-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b38c-125">NOTES</span></span>

## <span data-ttu-id="7b38c-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b38c-126">RELATED LINKS</span></span>

[<span data-ttu-id="7b38c-127">Add-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="7b38c-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="7b38c-128">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="7b38c-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="7b38c-129">Get-AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="7b38c-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


