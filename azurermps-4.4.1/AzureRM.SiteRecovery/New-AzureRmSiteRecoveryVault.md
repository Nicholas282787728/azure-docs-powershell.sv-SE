---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755914"
---
# <span data-ttu-id="b1b29-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="b1b29-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="b1b29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1b29-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b29-103">Skapar ett valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="b1b29-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1b29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1b29-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b29-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1b29-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b29-106">Cmdleten **New-AzureRmSiteRecoveryVault** skapar ett valv för Azure Site Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="b1b29-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="b1b29-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1b29-107">EXAMPLES</span></span>

## <span data-ttu-id="b1b29-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1b29-108">PARAMETERS</span></span>

### <span data-ttu-id="b1b29-109">-Plats</span><span class="sxs-lookup"><span data-stu-id="b1b29-109">-Location</span></span>
<span data-ttu-id="b1b29-110">Anger namnet på den geografiska platsen.</span><span class="sxs-lookup"><span data-stu-id="b1b29-110">Specifies the geographical location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b29-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="b1b29-111">-Name</span></span>
<span data-ttu-id="b1b29-112">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="b1b29-112">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b29-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b29-113">-ResourceGroupName</span></span>
<span data-ttu-id="b1b29-114">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b1b29-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b29-115">-DefaultProfile</span></span>
<span data-ttu-id="b1b29-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1b29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b29-117">CommonParameters</span></span>
<span data-ttu-id="b1b29-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b29-119">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b29-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b29-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1b29-120">INPUTS</span></span>

## <span data-ttu-id="b1b29-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1b29-121">OUTPUTS</span></span>

## <span data-ttu-id="b1b29-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1b29-122">NOTES</span></span>

## <span data-ttu-id="b1b29-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1b29-123">RELATED LINKS</span></span>

[<span data-ttu-id="b1b29-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="b1b29-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="b1b29-125">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="b1b29-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
