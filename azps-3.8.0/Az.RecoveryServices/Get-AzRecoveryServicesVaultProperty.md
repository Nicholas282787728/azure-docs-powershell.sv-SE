---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092441"
---
# <span data-ttu-id="42e81-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="42e81-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="42e81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="42e81-102">SYNOPSIS</span></span>
<span data-ttu-id="42e81-103">Returnerar egenskaperna för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="42e81-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="42e81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="42e81-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42e81-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="42e81-105">DESCRIPTION</span></span>
<span data-ttu-id="42e81-106">Cmdleten **Get-AzRecoveryServicesVaultProperty** returnerar egenskaperna för ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="42e81-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="42e81-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="42e81-107">EXAMPLES</span></span>

### <span data-ttu-id="42e81-108">Exempel 1: Hämta egenskaper för ett valv</span><span class="sxs-lookup"><span data-stu-id="42e81-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="42e81-109">Det första kommandot får ett valv objekt och lagrar det sedan i $vault variabel.</span><span class="sxs-lookup"><span data-stu-id="42e81-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="42e81-110">Det andra kommandot får egenskaperna för valvet.</span><span class="sxs-lookup"><span data-stu-id="42e81-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="42e81-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="42e81-111">PARAMETERS</span></span>

### <span data-ttu-id="42e81-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e81-112">-DefaultProfile</span></span>
<span data-ttu-id="42e81-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="42e81-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42e81-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="42e81-114">-VaultId</span></span>
<span data-ttu-id="42e81-115">ARM-ID för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="42e81-115">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42e81-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e81-116">CommonParameters</span></span>
<span data-ttu-id="42e81-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e81-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e81-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42e81-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e81-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="42e81-119">INPUTS</span></span>

### <span data-ttu-id="42e81-120">System. String</span><span class="sxs-lookup"><span data-stu-id="42e81-120">System.String</span></span>

## <span data-ttu-id="42e81-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="42e81-121">OUTPUTS</span></span>

### <span data-ttu-id="42e81-122">Microsoft. Azure. Management. RecoveryServices. backup. Models. BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="42e81-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="42e81-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="42e81-123">NOTES</span></span>

## <span data-ttu-id="42e81-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="42e81-124">RELATED LINKS</span></span>

[<span data-ttu-id="42e81-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="42e81-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="42e81-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="42e81-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
