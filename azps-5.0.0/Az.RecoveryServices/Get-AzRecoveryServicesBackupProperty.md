---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323046"
---
# <span data-ttu-id="cd313-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="cd313-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="cd313-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd313-102">SYNOPSIS</span></span>
<span data-ttu-id="cd313-103">Hämtar egenskaper för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="cd313-103">Gets Backup properties.</span></span>

## <span data-ttu-id="cd313-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd313-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd313-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd313-105">DESCRIPTION</span></span>
<span data-ttu-id="cd313-106">Cmdleten **Get-AzRecoveryServicesBackupProperty** hämtar säkerhets kopierings egenskaper för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="cd313-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="cd313-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd313-107">EXAMPLES</span></span>

### <span data-ttu-id="cd313-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd313-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="cd313-109">Skaffa säkerhets kopierings valv egenskapen för valvet.</span><span class="sxs-lookup"><span data-stu-id="cd313-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="cd313-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd313-110">PARAMETERS</span></span>

### <span data-ttu-id="cd313-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd313-111">-DefaultProfile</span></span>
<span data-ttu-id="cd313-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd313-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd313-113">-Valv</span><span class="sxs-lookup"><span data-stu-id="cd313-113">-Vault</span></span>
<span data-ttu-id="cd313-114">Anger namnet på valvet.</span><span class="sxs-lookup"><span data-stu-id="cd313-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="cd313-115">Valvet måste vara ett **AzureRmRecoveryServicesVault** -objekt.</span><span class="sxs-lookup"><span data-stu-id="cd313-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="cd313-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd313-116">CommonParameters</span></span>
<span data-ttu-id="cd313-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd313-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd313-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd313-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd313-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd313-119">INPUTS</span></span>

### <span data-ttu-id="cd313-120">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="cd313-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="cd313-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd313-121">OUTPUTS</span></span>

### <span data-ttu-id="cd313-122">Microsoft. Azure. commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="cd313-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="cd313-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd313-123">NOTES</span></span>

## <span data-ttu-id="cd313-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd313-124">RELATED LINKS</span></span>