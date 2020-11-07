---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756870"
---
# <span data-ttu-id="e4244-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e4244-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="e4244-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4244-102">SYNOPSIS</span></span>
<span data-ttu-id="e4244-103">Tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="e4244-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4244-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4244-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4244-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4244-105">DESCRIPTION</span></span>
<span data-ttu-id="e4244-106">Cmdleten **Remove-AzureRmRecoveryServicesVault** tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="e4244-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="e4244-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4244-107">EXAMPLES</span></span>

## <span data-ttu-id="e4244-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4244-108">PARAMETERS</span></span>

### <span data-ttu-id="e4244-109">-Valv</span><span class="sxs-lookup"><span data-stu-id="e4244-109">-Vault</span></span>
<span data-ttu-id="e4244-110">Anger ett objekt för Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="e4244-110">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="e4244-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e4244-111">-Confirm</span></span>
<span data-ttu-id="e4244-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e4244-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4244-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4244-113">-WhatIf</span></span>
<span data-ttu-id="e4244-114">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e4244-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4244-115">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e4244-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4244-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4244-116">-DefaultProfile</span></span>
<span data-ttu-id="e4244-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4244-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4244-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4244-118">CommonParameters</span></span>
<span data-ttu-id="e4244-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4244-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4244-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4244-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4244-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4244-121">INPUTS</span></span>

### <span data-ttu-id="e4244-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="e4244-122">ARSVault</span></span>
<span data-ttu-id="e4244-123">Parametern ' valv ' godkänner värdet av typen ' ARSVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e4244-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="e4244-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4244-124">OUTPUTS</span></span>

### <span data-ttu-id="e4244-125">Microsoft. Azure. commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="e4244-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="e4244-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4244-126">NOTES</span></span>

## <span data-ttu-id="e4244-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4244-127">RELATED LINKS</span></span>

[<span data-ttu-id="e4244-128">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e4244-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="e4244-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e4244-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e4244-130">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e4244-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


