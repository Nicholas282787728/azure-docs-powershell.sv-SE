---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757202"
---
# <span data-ttu-id="5524e-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5524e-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="5524e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5524e-102">SYNOPSIS</span></span>
<span data-ttu-id="5524e-103">Hämtar Site Recovery-valv från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5524e-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5524e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5524e-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5524e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5524e-105">DESCRIPTION</span></span>
<span data-ttu-id="5524e-106">Cmdleten **Get-AzureRmSiteRecoveryVault** hämtar en lista med Azure Site Recovery-valv eller ett specifikt webbplats återställnings valv från det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="5524e-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="5524e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5524e-107">EXAMPLES</span></span>

## <span data-ttu-id="5524e-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5524e-108">PARAMETERS</span></span>

### <span data-ttu-id="5524e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5524e-109">-DefaultProfile</span></span>
<span data-ttu-id="5524e-110">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5524e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5524e-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="5524e-111">-Name</span></span>
<span data-ttu-id="5524e-112">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="5524e-112">Specifies the name of the vault.</span></span>

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

### <span data-ttu-id="5524e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5524e-113">-ResourceGroupName</span></span>
<span data-ttu-id="5524e-114">Anger namnet på den Azure Resource-grupp som du vill hämta Recovery Services-objektet från.</span><span class="sxs-lookup"><span data-stu-id="5524e-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

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

### <span data-ttu-id="5524e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5524e-115">CommonParameters</span></span>
<span data-ttu-id="5524e-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5524e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5524e-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5524e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5524e-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5524e-118">INPUTS</span></span>

### <span data-ttu-id="5524e-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="5524e-119">None</span></span>
<span data-ttu-id="5524e-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="5524e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5524e-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5524e-121">OUTPUTS</span></span>

### <span data-ttu-id="5524e-122">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="5524e-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="5524e-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5524e-123">NOTES</span></span>

## <span data-ttu-id="5524e-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5524e-124">RELATED LINKS</span></span>

[<span data-ttu-id="5524e-125">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5524e-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="5524e-126">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5524e-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
