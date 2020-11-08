---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088625"
---
# <span data-ttu-id="2aa87-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="2aa87-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="2aa87-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2aa87-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa87-103">Hämtar information om inställningar för ASR-valv för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="2aa87-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="2aa87-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2aa87-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aa87-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2aa87-105">DESCRIPTION</span></span>
<span data-ttu-id="2aa87-106">Cmdleten **Get-AzRecoveryServicesAsrVaultContext** hämtar information om inställningar för ASR-valv relaterade till Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="2aa87-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="2aa87-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2aa87-107">EXAMPLES</span></span>

### <span data-ttu-id="2aa87-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2aa87-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="2aa87-109">Hämtar inställningar för ASR-valv för det aktiva (i PowerShell-sessionen) Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="2aa87-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="2aa87-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2aa87-110">PARAMETERS</span></span>

### <span data-ttu-id="2aa87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa87-111">-DefaultProfile</span></span>
<span data-ttu-id="2aa87-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa87-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa87-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa87-113">CommonParameters</span></span>
<span data-ttu-id="2aa87-114">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa87-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa87-115">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aa87-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa87-116">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2aa87-116">INPUTS</span></span>

### <span data-ttu-id="2aa87-117">Ingen</span><span class="sxs-lookup"><span data-stu-id="2aa87-117">None</span></span>

## <span data-ttu-id="2aa87-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2aa87-118">OUTPUTS</span></span>

### <span data-ttu-id="2aa87-119">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="2aa87-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="2aa87-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2aa87-120">NOTES</span></span>

## <span data-ttu-id="2aa87-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2aa87-121">RELATED LINKS</span></span>
