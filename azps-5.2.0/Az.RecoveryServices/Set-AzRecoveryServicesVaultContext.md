---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415408"
---
# <span data-ttu-id="1899d-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="1899d-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="1899d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1899d-102">SYNOPSIS</span></span>

<span data-ttu-id="1899d-103">Anger valv kontext.</span><span class="sxs-lookup"><span data-stu-id="1899d-103">Sets vault context.</span></span>

## <span data-ttu-id="1899d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1899d-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1899d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1899d-105">DESCRIPTION</span></span>

<span data-ttu-id="1899d-106">Cmdleten **set-AzRecoveryServicesVaultContext** anger valv kontexten för Azure Site Recovery-tjänsterna.</span><span class="sxs-lookup"><span data-stu-id="1899d-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="1899d-107">Varning! den här cmdleten är föråldrad i en framtida brytar ändrings version.</span><span class="sxs-lookup"><span data-stu-id="1899d-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="1899d-108">Det kommer inte att ersätta det.</span><span class="sxs-lookup"><span data-stu-id="1899d-108">There will be no replacement for it.</span></span> <span data-ttu-id="1899d-109">Använd parametern-VaultId i alla Recovery Services-kommandon som skickas.</span><span class="sxs-lookup"><span data-stu-id="1899d-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="1899d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1899d-110">EXAMPLES</span></span>

### <span data-ttu-id="1899d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1899d-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="1899d-112">Anger valv kontext.</span><span class="sxs-lookup"><span data-stu-id="1899d-112">Sets vault context.</span></span>

## <span data-ttu-id="1899d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1899d-113">PARAMETERS</span></span>

### <span data-ttu-id="1899d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1899d-114">-DefaultProfile</span></span>

<span data-ttu-id="1899d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1899d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1899d-116">-Valv</span><span class="sxs-lookup"><span data-stu-id="1899d-116">-Vault</span></span>

<span data-ttu-id="1899d-117">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="1899d-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="1899d-118">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1899d-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="1899d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1899d-119">CommonParameters</span></span>
<span data-ttu-id="1899d-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1899d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1899d-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1899d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1899d-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1899d-122">INPUTS</span></span>

### <span data-ttu-id="1899d-123">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="1899d-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="1899d-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1899d-124">OUTPUTS</span></span>

### <span data-ttu-id="1899d-125">System. Void</span><span class="sxs-lookup"><span data-stu-id="1899d-125">System.Void</span></span>

## <span data-ttu-id="1899d-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1899d-126">NOTES</span></span>

## <span data-ttu-id="1899d-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1899d-127">RELATED LINKS</span></span>
