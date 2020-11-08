---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099552"
---
# <span data-ttu-id="514bc-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="514bc-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="514bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="514bc-102">SYNOPSIS</span></span>
<span data-ttu-id="514bc-103">Hämtar resultatet från en Azure RemoteApp-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="514bc-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="514bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="514bc-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="514bc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="514bc-105">DESCRIPTION</span></span>
<span data-ttu-id="514bc-106">Cmdleten **Get-AzureRemoteAppOperationResult** returnerar resultatet av en Azure RemoteApp-åtgärd som körs längre.</span><span class="sxs-lookup"><span data-stu-id="514bc-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="514bc-107">Azure RemoteApp använder långa drifts operationer för många åtgärder som kräver bearbetning av tjänsten och kan inte gå tillbaka omedelbart.</span><span class="sxs-lookup"><span data-stu-id="514bc-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="514bc-108">Exempel på cmdlets som returnerar uppföljnings-ID: n är **Update-AzureRemoteAppCollection** , **set-AzureRemoteAppWorkspace** , **disconnect-AzureRemoteAppSession** och andra.</span><span class="sxs-lookup"><span data-stu-id="514bc-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="514bc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="514bc-109">EXAMPLES</span></span>

### <span data-ttu-id="514bc-110">Exempel 1: använda ett uppföljnings-ID för att få ett åtgärds resultat</span><span class="sxs-lookup"><span data-stu-id="514bc-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="514bc-111">Det här kommandot sparar det uppföljnings-ID som returneras från en Azure RemoteApp-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="514bc-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="514bc-112">Spårnings-ID: t skickas till **Get-AzureRemoteAppOperationResult** i det kommando som följer.</span><span class="sxs-lookup"><span data-stu-id="514bc-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="514bc-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="514bc-113">PARAMETERS</span></span>

### <span data-ttu-id="514bc-114">-Profil</span><span class="sxs-lookup"><span data-stu-id="514bc-114">-Profile</span></span>
<span data-ttu-id="514bc-115">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="514bc-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="514bc-116">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="514bc-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="514bc-117">-TrackingId</span><span class="sxs-lookup"><span data-stu-id="514bc-117">-TrackingId</span></span>
<span data-ttu-id="514bc-118">Anger spårnings-ID för en åtgärd.</span><span class="sxs-lookup"><span data-stu-id="514bc-118">Specifies the tracking ID of an operation.</span></span>

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

### <span data-ttu-id="514bc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="514bc-119">CommonParameters</span></span>
<span data-ttu-id="514bc-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="514bc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="514bc-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="514bc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="514bc-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="514bc-122">INPUTS</span></span>

## <span data-ttu-id="514bc-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="514bc-123">OUTPUTS</span></span>

## <span data-ttu-id="514bc-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="514bc-124">NOTES</span></span>

## <span data-ttu-id="514bc-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="514bc-125">RELATED LINKS</span></span>

[<span data-ttu-id="514bc-126">Koppla från-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="514bc-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="514bc-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="514bc-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="514bc-128">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="514bc-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


