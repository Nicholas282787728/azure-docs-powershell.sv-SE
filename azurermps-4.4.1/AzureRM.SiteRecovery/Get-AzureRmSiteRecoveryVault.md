---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756846"
---
# <span data-ttu-id="8d990-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8d990-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="8d990-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d990-102">SYNOPSIS</span></span>
<span data-ttu-id="8d990-103">Hämtar Site Recovery-valv från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8d990-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d990-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d990-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d990-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d990-105">DESCRIPTION</span></span>
<span data-ttu-id="8d990-106">Cmdleten **Get-AzureRmSiteRecoveryVault** hämtar en lista med Azure Site Recovery-valv eller ett specifikt webbplats återställnings valv från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8d990-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="8d990-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d990-107">EXAMPLES</span></span>

## <span data-ttu-id="8d990-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d990-108">PARAMETERS</span></span>

### <span data-ttu-id="8d990-109">-Namn</span><span class="sxs-lookup"><span data-stu-id="8d990-109">-Name</span></span>
<span data-ttu-id="8d990-110">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="8d990-110">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d990-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d990-111">-ResourceGroupName</span></span>
<span data-ttu-id="8d990-112">Anger namnet på den Azure Resource-grupp som du vill hämta Recovery Services-objektet från.</span><span class="sxs-lookup"><span data-stu-id="8d990-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d990-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d990-113">-DefaultProfile</span></span>
<span data-ttu-id="8d990-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d990-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d990-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d990-115">CommonParameters</span></span>
<span data-ttu-id="8d990-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d990-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d990-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d990-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d990-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d990-118">INPUTS</span></span>

## <span data-ttu-id="8d990-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d990-119">OUTPUTS</span></span>

### <span data-ttu-id="8d990-120">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="8d990-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="8d990-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d990-121">NOTES</span></span>

## <span data-ttu-id="8d990-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d990-122">RELATED LINKS</span></span>

[<span data-ttu-id="8d990-123">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8d990-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="8d990-124">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="8d990-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
