---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099376"
---
# <span data-ttu-id="483c3-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="483c3-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="483c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="483c3-102">SYNOPSIS</span></span>
<span data-ttu-id="483c3-103">Tar bort ett Azure RemoteApp-nätverk.</span><span class="sxs-lookup"><span data-stu-id="483c3-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="483c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="483c3-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="483c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="483c3-105">DESCRIPTION</span></span>
<span data-ttu-id="483c3-106">Cmdleten **Remove-AzureRemoteAppVNet** tar bort ett Azure RemoteApp-nätverk.</span><span class="sxs-lookup"><span data-stu-id="483c3-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="483c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="483c3-107">EXAMPLES</span></span>

### <span data-ttu-id="483c3-108">Exempel 1: ta bort ett angivet virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="483c3-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="483c3-109">Det här kommandot tar bort det virtuella nätverket med namnet ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="483c3-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="483c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="483c3-110">PARAMETERS</span></span>

### <span data-ttu-id="483c3-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="483c3-111">-Profile</span></span>
<span data-ttu-id="483c3-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="483c3-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="483c3-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="483c3-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="483c3-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="483c3-114">-VNetName</span></span>
<span data-ttu-id="483c3-115">Anger namnet på det virtuella Azure RemoteApp-nätverket som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="483c3-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="483c3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483c3-116">CommonParameters</span></span>
<span data-ttu-id="483c3-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483c3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483c3-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="483c3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483c3-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="483c3-119">INPUTS</span></span>

## <span data-ttu-id="483c3-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="483c3-120">OUTPUTS</span></span>

## <span data-ttu-id="483c3-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="483c3-121">NOTES</span></span>

## <span data-ttu-id="483c3-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="483c3-122">RELATED LINKS</span></span>

[<span data-ttu-id="483c3-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="483c3-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="483c3-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="483c3-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


