---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747330"
---
# <span data-ttu-id="6f9b1-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="6f9b1-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="6f9b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f9b1-102">SYNOPSIS</span></span>
<span data-ttu-id="6f9b1-103">Anger valv kontext.</span><span class="sxs-lookup"><span data-stu-id="6f9b1-103">Sets vault context.</span></span>

## <span data-ttu-id="6f9b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f9b1-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f9b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f9b1-105">DESCRIPTION</span></span>
<span data-ttu-id="6f9b1-106">Cmdleten **set-AzRecoveryServicesVaultContext** anger valv kontexten för Azure Site Recovery-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="6f9b1-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="6f9b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f9b1-107">EXAMPLES</span></span>

### <span data-ttu-id="6f9b1-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6f9b1-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="6f9b1-109">Anger valv kontext.</span><span class="sxs-lookup"><span data-stu-id="6f9b1-109">Sets vault context.</span></span>

## <span data-ttu-id="6f9b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f9b1-110">PARAMETERS</span></span>

### <span data-ttu-id="6f9b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f9b1-111">-DefaultProfile</span></span>
<span data-ttu-id="6f9b1-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f9b1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f9b1-113">-Valv</span><span class="sxs-lookup"><span data-stu-id="6f9b1-113">-Vault</span></span>
<span data-ttu-id="6f9b1-114">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="6f9b1-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="6f9b1-115">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6f9b1-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f9b1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f9b1-116">CommonParameters</span></span>
<span data-ttu-id="6f9b1-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f9b1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f9b1-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f9b1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f9b1-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f9b1-119">INPUTS</span></span>

### <span data-ttu-id="6f9b1-120">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="6f9b1-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6f9b1-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f9b1-121">OUTPUTS</span></span>

### <span data-ttu-id="6f9b1-122">System. Void</span><span class="sxs-lookup"><span data-stu-id="6f9b1-122">System.Void</span></span>

## <span data-ttu-id="6f9b1-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f9b1-123">NOTES</span></span>

## <span data-ttu-id="6f9b1-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f9b1-124">RELATED LINKS</span></span>