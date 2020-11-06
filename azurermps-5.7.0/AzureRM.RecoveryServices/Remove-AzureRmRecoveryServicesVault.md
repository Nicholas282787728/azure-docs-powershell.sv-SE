---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581024"
---
# <span data-ttu-id="a2d70-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a2d70-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="a2d70-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a2d70-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d70-103">Tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="a2d70-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2d70-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a2d70-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d70-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a2d70-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d70-106">Cmdleten **Remove-AzureRmRecoveryServicesVault** tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="a2d70-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a2d70-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a2d70-107">EXAMPLES</span></span>

### <span data-ttu-id="a2d70-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a2d70-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="a2d70-109">Tar bort ett Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="a2d70-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a2d70-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a2d70-110">PARAMETERS</span></span>

### <span data-ttu-id="a2d70-111">-Valv</span><span class="sxs-lookup"><span data-stu-id="a2d70-111">-Vault</span></span>
<span data-ttu-id="a2d70-112">Anger ett objekt för Azure Site Recovery-valv.</span><span class="sxs-lookup"><span data-stu-id="a2d70-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="a2d70-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a2d70-113">-Confirm</span></span>
<span data-ttu-id="a2d70-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a2d70-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d70-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d70-115">-WhatIf</span></span>
<span data-ttu-id="a2d70-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a2d70-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2d70-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a2d70-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d70-118">-DefaultProfile</span></span>
<span data-ttu-id="a2d70-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d70-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d70-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d70-120">CommonParameters</span></span>
<span data-ttu-id="a2d70-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d70-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d70-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d70-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d70-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a2d70-123">INPUTS</span></span>

### <span data-ttu-id="a2d70-124">ARSVault</span><span class="sxs-lookup"><span data-stu-id="a2d70-124">ARSVault</span></span>
<span data-ttu-id="a2d70-125">Parametern ' valv ' godkänner värdet av typen ' ARSVault ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a2d70-125">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="a2d70-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a2d70-126">OUTPUTS</span></span>

### <span data-ttu-id="a2d70-127">Microsoft. Azure. commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="a2d70-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="a2d70-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a2d70-128">NOTES</span></span>

## <span data-ttu-id="a2d70-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a2d70-129">RELATED LINKS</span></span>

[<span data-ttu-id="a2d70-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a2d70-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="a2d70-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a2d70-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a2d70-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a2d70-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


