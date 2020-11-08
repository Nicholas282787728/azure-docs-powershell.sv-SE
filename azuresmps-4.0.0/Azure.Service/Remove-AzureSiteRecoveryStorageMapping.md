---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099339"
---
# <span data-ttu-id="18f52-101">Remove-AzureSiteRecoveryStorageMapping</span><span class="sxs-lookup"><span data-stu-id="18f52-101">Remove-AzureSiteRecoveryStorageMapping</span></span>

## <span data-ttu-id="18f52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18f52-102">SYNOPSIS</span></span>
<span data-ttu-id="18f52-103">Tar bort en mappning för lagrings objekt för ett återställnings valv för webbplatser.</span><span class="sxs-lookup"><span data-stu-id="18f52-103">Removes a Storage object mapping for a Site Recovery vault.</span></span>

## <span data-ttu-id="18f52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18f52-104">SYNTAX</span></span>

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="18f52-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18f52-105">DESCRIPTION</span></span>
<span data-ttu-id="18f52-106">Cmdleten **Remove-AzureSiteRecoveryStorageMapping** tar bort en lagrings objekt mappning för det aktuella Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="18f52-106">The **Remove-AzureSiteRecoveryStorageMapping** cmdlet removes a Storage object mapping for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="18f52-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18f52-107">EXAMPLES</span></span>

### <span data-ttu-id="18f52-108">Exempel 1: ta bort mappningen mellan ett nätverk och ett återställnings nätverk</span><span class="sxs-lookup"><span data-stu-id="18f52-108">Example 1: Remove the mapping between a network and a recovery network</span></span>
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

<span data-ttu-id="18f52-109">Den första kommando cmdleten hämtar servrar för det aktuella Azure Site Recovery-valvet med cmdleten **Get-AzureSiteRecoveryServer** .</span><span class="sxs-lookup"><span data-stu-id="18f52-109">The first command cmdlet gets servers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryServer** cmdlet.</span></span>
<span data-ttu-id="18f52-110">Kommandot lagrar webbplats återställnings servrarna i $Servers mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="18f52-110">The command stores the Site Recovery servers in the $Servers array variable.</span></span>

<span data-ttu-id="18f52-111">Det andra kommandot får mappningen mellan två lagrings objekt och lagrar det sedan i $StorageMapping variabel.</span><span class="sxs-lookup"><span data-stu-id="18f52-111">The second command gets the mapping between two Storage objects, and then stores it in the $StorageMapping variable.</span></span>
<span data-ttu-id="18f52-112">Kommandot anger den primära servern för nätverks mappningen som det första elementet i $Servers.</span><span class="sxs-lookup"><span data-stu-id="18f52-112">The command specifies the primary server for the network mapping as the first element of $Servers.</span></span>
<span data-ttu-id="18f52-113">Kommandot anger Server för återställnings nätverket som det andra $Servers.</span><span class="sxs-lookup"><span data-stu-id="18f52-113">The command specifies the server for the recovery network as the second element of $Servers.</span></span>

<span data-ttu-id="18f52-114">Kommandot tar bort mappningen i $StorageMapping.</span><span class="sxs-lookup"><span data-stu-id="18f52-114">The final command removes the mapping in $StorageMapping.</span></span>

## <span data-ttu-id="18f52-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18f52-115">PARAMETERS</span></span>

### <span data-ttu-id="18f52-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="18f52-116">-Profile</span></span>
<span data-ttu-id="18f52-117">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="18f52-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="18f52-118">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="18f52-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="18f52-119">-StorageMapping</span><span class="sxs-lookup"><span data-stu-id="18f52-119">-StorageMapping</span></span>
<span data-ttu-id="18f52-120">Anger en nätverks mappning.</span><span class="sxs-lookup"><span data-stu-id="18f52-120">Specifies a network mapping.</span></span>
<span data-ttu-id="18f52-121">För att få en **ASRStorageMapping** använder du cmdleten **Get-AzureSiteRecoveryStorage** .</span><span class="sxs-lookup"><span data-stu-id="18f52-121">To obtain an **ASRStorageMapping** , use the **Get-AzureSiteRecoveryStorage** cmdlet.</span></span>

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18f52-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18f52-122">CommonParameters</span></span>
<span data-ttu-id="18f52-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18f52-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18f52-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18f52-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18f52-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18f52-125">INPUTS</span></span>

## <span data-ttu-id="18f52-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18f52-126">OUTPUTS</span></span>

## <span data-ttu-id="18f52-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18f52-127">NOTES</span></span>

## <span data-ttu-id="18f52-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18f52-128">RELATED LINKS</span></span>

[<span data-ttu-id="18f52-129">Get-AzureSiteRecoveryStorage</span><span class="sxs-lookup"><span data-stu-id="18f52-129">Get-AzureSiteRecoveryStorage</span></span>](./Get-AzureSiteRecoveryStorage.md)


