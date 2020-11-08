---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091267"
---
# <span data-ttu-id="e60d9-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e60d9-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="e60d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e60d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e60d9-103">Tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="e60d9-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="e60d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e60d9-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e60d9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e60d9-105">DESCRIPTION</span></span>
<span data-ttu-id="e60d9-106">Cmdleten **Remove-AzRecoveryServicesVault** tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="e60d9-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="e60d9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e60d9-107">EXAMPLES</span></span>

### <span data-ttu-id="e60d9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e60d9-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="e60d9-109">Tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="e60d9-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="e60d9-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e60d9-110">PARAMETERS</span></span>

### <span data-ttu-id="e60d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60d9-111">-DefaultProfile</span></span>
<span data-ttu-id="e60d9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e60d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e60d9-113">-Valv</span><span class="sxs-lookup"><span data-stu-id="e60d9-113">-Vault</span></span>
<span data-ttu-id="e60d9-114">Anger ett objekt för Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="e60d9-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="e60d9-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e60d9-115">-Confirm</span></span>
<span data-ttu-id="e60d9-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e60d9-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60d9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e60d9-117">-WhatIf</span></span>
<span data-ttu-id="e60d9-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e60d9-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e60d9-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e60d9-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e60d9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60d9-120">CommonParameters</span></span>
<span data-ttu-id="e60d9-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e60d9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60d9-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e60d9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60d9-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e60d9-123">INPUTS</span></span>

### <span data-ttu-id="e60d9-124">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e60d9-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e60d9-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e60d9-125">OUTPUTS</span></span>

### <span data-ttu-id="e60d9-126">Microsoft. Azure. commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="e60d9-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="e60d9-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e60d9-127">NOTES</span></span>

## <span data-ttu-id="e60d9-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e60d9-128">RELATED LINKS</span></span>

[<span data-ttu-id="e60d9-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e60d9-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="e60d9-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e60d9-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e60d9-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e60d9-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

