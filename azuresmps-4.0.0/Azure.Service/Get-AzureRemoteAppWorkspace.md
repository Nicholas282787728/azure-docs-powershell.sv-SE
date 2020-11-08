---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093345"
---
# <span data-ttu-id="2bee4-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="2bee4-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="2bee4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bee4-102">SYNOPSIS</span></span>
<span data-ttu-id="2bee4-103">Hämtar information om en Azure RemoteApp-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="2bee4-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="2bee4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bee4-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2bee4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bee4-105">DESCRIPTION</span></span>
<span data-ttu-id="2bee4-106">Cmdleten **Get-AzureRemoteAppWorkspace** hämtar information om en Azure RemoteApp-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="2bee4-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="2bee4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bee4-107">EXAMPLES</span></span>

### <span data-ttu-id="2bee4-108">Exempel 1: Hämta information om en arbets yta</span><span class="sxs-lookup"><span data-stu-id="2bee4-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="2bee4-109">Det här kommandot hämtar information om Azure RemoteApp-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="2bee4-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="2bee4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bee4-110">PARAMETERS</span></span>

### <span data-ttu-id="2bee4-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="2bee4-111">-Profile</span></span>
<span data-ttu-id="2bee4-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="2bee4-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2bee4-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="2bee4-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2bee4-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bee4-114">CommonParameters</span></span>
<span data-ttu-id="2bee4-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bee4-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bee4-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bee4-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bee4-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bee4-117">INPUTS</span></span>

## <span data-ttu-id="2bee4-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bee4-118">OUTPUTS</span></span>

## <span data-ttu-id="2bee4-119">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bee4-119">NOTES</span></span>

## <span data-ttu-id="2bee4-120">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bee4-120">RELATED LINKS</span></span>

[<span data-ttu-id="2bee4-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="2bee4-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)


