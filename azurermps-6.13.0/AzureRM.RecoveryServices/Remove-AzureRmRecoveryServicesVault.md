---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: e6ac59a84e4244cb6d6815f8e3256618cccd661c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584011"
---
# <span data-ttu-id="8d0d6-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8d0d6-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="8d0d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8d0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="8d0d6-103">Tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d0d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8d0d6-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d0d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8d0d6-105">DESCRIPTION</span></span>
<span data-ttu-id="8d0d6-106">Cmdleten **Remove-AzureRmRecoveryServicesVault** tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="8d0d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8d0d6-107">EXAMPLES</span></span>

### <span data-ttu-id="8d0d6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8d0d6-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="8d0d6-109">Tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="8d0d6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8d0d6-110">PARAMETERS</span></span>

### <span data-ttu-id="8d0d6-111">-Valv</span><span class="sxs-lookup"><span data-stu-id="8d0d6-111">-Vault</span></span>
<span data-ttu-id="8d0d6-112">Anger ett objekt för Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-112">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d6-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8d0d6-113">-Confirm</span></span>
<span data-ttu-id="8d0d6-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d6-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d0d6-115">-WhatIf</span></span>
<span data-ttu-id="8d0d6-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d0d6-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d0d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d0d6-118">-DefaultProfile</span></span>
<span data-ttu-id="8d0d6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d0d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d0d6-120">CommonParameters</span></span>
<span data-ttu-id="8d0d6-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d0d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d0d6-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d0d6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d0d6-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8d0d6-123">INPUTS</span></span>

### <span data-ttu-id="8d0d6-124">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="8d0d6-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="8d0d6-125">Parametrar: valv (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8d0d6-125">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="8d0d6-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8d0d6-126">OUTPUTS</span></span>

### <span data-ttu-id="8d0d6-127">Microsoft. Azure. commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="8d0d6-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="8d0d6-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8d0d6-128">NOTES</span></span>

## <span data-ttu-id="8d0d6-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8d0d6-129">RELATED LINKS</span></span>

[<span data-ttu-id="8d0d6-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8d0d6-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="8d0d6-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="8d0d6-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="8d0d6-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="8d0d6-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


