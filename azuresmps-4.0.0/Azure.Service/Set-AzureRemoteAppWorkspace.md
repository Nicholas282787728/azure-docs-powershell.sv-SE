---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099281"
---
# <span data-ttu-id="3774a-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="3774a-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="3774a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3774a-102">SYNOPSIS</span></span>
<span data-ttu-id="3774a-103">Anger egenskaper för en Azure RemoteApp-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="3774a-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="3774a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3774a-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3774a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3774a-105">DESCRIPTION</span></span>
<span data-ttu-id="3774a-106">Cmdleten **set-AzureRemoteAppWorkspace** anger egenskaperna för en Azure RemoteApp-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="3774a-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="3774a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3774a-107">EXAMPLES</span></span>

### <span data-ttu-id="3774a-108">Exempel 1: Ange arbets ytans namn</span><span class="sxs-lookup"><span data-stu-id="3774a-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="3774a-109">Det här kommandot anger namnet på en Azure RemoteApp-arbetsyta till contoso-arbetsprogram.</span><span class="sxs-lookup"><span data-stu-id="3774a-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="3774a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3774a-110">PARAMETERS</span></span>

### <span data-ttu-id="3774a-111">-Profil</span><span class="sxs-lookup"><span data-stu-id="3774a-111">-Profile</span></span>
<span data-ttu-id="3774a-112">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="3774a-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3774a-113">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="3774a-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3774a-114">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3774a-114">-WorkspaceName</span></span>
<span data-ttu-id="3774a-115">Anger namnet på Azure RemoteApp-arbetsytan.</span><span class="sxs-lookup"><span data-stu-id="3774a-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3774a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3774a-116">CommonParameters</span></span>
<span data-ttu-id="3774a-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3774a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3774a-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3774a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3774a-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3774a-119">INPUTS</span></span>

## <span data-ttu-id="3774a-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3774a-120">OUTPUTS</span></span>

## <span data-ttu-id="3774a-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3774a-121">NOTES</span></span>
* <span data-ttu-id="3774a-122">Alla Azure RemoteApp-samlingar för ett angivet abonnemang finns i en delad arbets yta.</span><span class="sxs-lookup"><span data-stu-id="3774a-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="3774a-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3774a-123">RELATED LINKS</span></span>

[<span data-ttu-id="3774a-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="3774a-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)


