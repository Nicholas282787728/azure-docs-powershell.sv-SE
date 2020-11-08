---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 4E19A767-8233-42A0-95C5-1547B4DF297E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67c08105f8083b6b2e132c3b8e61c92627572305
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099564"
---
# <span data-ttu-id="d0bba-101">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d0bba-101">Get-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="d0bba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0bba-102">SYNOPSIS</span></span>
<span data-ttu-id="d0bba-103">Hämtar information om en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="d0bba-103">Gets details for a network security group.</span></span>

## <span data-ttu-id="d0bba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0bba-104">SYNTAX</span></span>

```
Get-AzureNetworkSecurityGroup [-Name <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d0bba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0bba-105">DESCRIPTION</span></span>
<span data-ttu-id="d0bba-106">Cmdleten **Get-AzureNetworkSecurityGroup** returnerar information om en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="d0bba-106">The **Get-AzureNetworkSecurityGroup** cmdlet returns details for an Azure network security group.</span></span>
<span data-ttu-id="d0bba-107">Ange en *detaljerad* parameter för att Visa nätverks säkerhets reglerna.</span><span class="sxs-lookup"><span data-stu-id="d0bba-107">Specify the *Detailed* parameter to display the network security rules.</span></span>

## <span data-ttu-id="d0bba-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0bba-108">EXAMPLES</span></span>

## <span data-ttu-id="d0bba-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0bba-109">PARAMETERS</span></span>

### <span data-ttu-id="d0bba-110">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="d0bba-110">-Detailed</span></span>
<span data-ttu-id="d0bba-111">Anger att denna cmdlet returnerar nätverks säkerhets reglerna för nätverks säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="d0bba-111">Indicates that this cmdlet returns the network security rules for the network security group.</span></span>

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

### <span data-ttu-id="d0bba-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0bba-112">-Name</span></span>
<span data-ttu-id="d0bba-113">Anger namnet på den nätverks säkerhets grupp som den här cmdleten får.</span><span class="sxs-lookup"><span data-stu-id="d0bba-113">Specifies the name of the network security group that this cmdlet gets.</span></span>

> [!NOTE]
> <span data-ttu-id="d0bba-114">När en klassisk nätverks säkerhets grupp skapas i en annan resurs grupp än ***standard-nätverk*** med Azure-portalen måste du använda följande PowerShell-syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'` .</span><span class="sxs-lookup"><span data-stu-id="d0bba-114">When a classic network security group is created in a resource group other than ***Default-Networking*** using the Azure portal, you must use the following PowerShell syntax: `Get-AzureNetworkSecurityGroup -Name 'Group myResouceGroup myNetworkSecurityGroup'`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0bba-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="d0bba-115">-Profile</span></span>
<span data-ttu-id="d0bba-116">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="d0bba-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d0bba-117">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="d0bba-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d0bba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0bba-118">CommonParameters</span></span>
<span data-ttu-id="d0bba-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0bba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0bba-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0bba-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0bba-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0bba-121">INPUTS</span></span>

## <span data-ttu-id="d0bba-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0bba-122">OUTPUTS</span></span>

## <span data-ttu-id="d0bba-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0bba-123">NOTES</span></span>

## <span data-ttu-id="d0bba-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0bba-124">RELATED LINKS</span></span>

[<span data-ttu-id="d0bba-125">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d0bba-125">New-AzureNetworkSecurityGroup</span></span>](./New-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="d0bba-126">Remove-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d0bba-126">Remove-AzureNetworkSecurityGroup</span></span>](./Remove-AzureNetworkSecurityGroup.md)

