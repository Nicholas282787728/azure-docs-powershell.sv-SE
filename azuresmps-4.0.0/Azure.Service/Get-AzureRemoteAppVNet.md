---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099800"
---
# <span data-ttu-id="473c7-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="473c7-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="473c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="473c7-102">SYNOPSIS</span></span>
<span data-ttu-id="473c7-103">Hämtar information om virtuella Azure RemoteApp-nätverk i Azure.</span><span class="sxs-lookup"><span data-stu-id="473c7-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="473c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="473c7-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="473c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="473c7-105">DESCRIPTION</span></span>
<span data-ttu-id="473c7-106">Cmdleten **Get-AzureRemoteAppVNet** hämtar information om virtuella Azure RemoteApp-nätverk i Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="473c7-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="473c7-107">Denna cmdlet returnerar ett objekt som innehåller information om ett angivet virtuellt nätverk.</span><span class="sxs-lookup"><span data-stu-id="473c7-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="473c7-108">Om inget virtuellt nätverk anges returnerar denna cmdlet information om alla virtuella nätverk i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="473c7-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="473c7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="473c7-109">EXAMPLES</span></span>

### <span data-ttu-id="473c7-110">Exempel 1: Hämta information om ett virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="473c7-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="473c7-111">Med det här kommandot får du information om det virtuella nätverket som heter ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="473c7-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="473c7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="473c7-112">PARAMETERS</span></span>

### <span data-ttu-id="473c7-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="473c7-113">-IncludeSharedKey</span></span>
<span data-ttu-id="473c7-114">Anger att den här cmdleten innehåller värdet för den delade lösningen i den information som hämtas om det virtuella nätverket.</span><span class="sxs-lookup"><span data-stu-id="473c7-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

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

### <span data-ttu-id="473c7-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="473c7-115">-Profile</span></span>
<span data-ttu-id="473c7-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="473c7-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="473c7-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="473c7-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="473c7-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="473c7-118">-VNetName</span></span>
<span data-ttu-id="473c7-119">Anger namnet på det virtuella Azure RemoteApp-nätverket.</span><span class="sxs-lookup"><span data-stu-id="473c7-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="473c7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="473c7-120">CommonParameters</span></span>
<span data-ttu-id="473c7-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="473c7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="473c7-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="473c7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="473c7-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="473c7-123">INPUTS</span></span>

## <span data-ttu-id="473c7-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="473c7-124">OUTPUTS</span></span>

## <span data-ttu-id="473c7-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="473c7-125">NOTES</span></span>

## <span data-ttu-id="473c7-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="473c7-126">RELATED LINKS</span></span>

[<span data-ttu-id="473c7-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="473c7-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


