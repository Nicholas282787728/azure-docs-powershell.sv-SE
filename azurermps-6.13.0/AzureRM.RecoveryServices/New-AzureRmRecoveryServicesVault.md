---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 08166ea1ebe4c78521a68f9e5423a7947e78b699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584012"
---
# <span data-ttu-id="99195-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="99195-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="99195-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99195-102">SYNOPSIS</span></span>
<span data-ttu-id="99195-103">Skapar ett nytt Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="99195-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99195-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99195-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99195-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99195-105">DESCRIPTION</span></span>
<span data-ttu-id="99195-106">Cmdleten **New-AzureRmRecoveryServicesVault** skapar ett nytt Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="99195-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="99195-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99195-107">EXAMPLES</span></span>

### <span data-ttu-id="99195-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="99195-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="99195-109">Skapa ett valv för återställnings tjänster i resurs gruppen och den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="99195-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="99195-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99195-110">PARAMETERS</span></span>

### <span data-ttu-id="99195-111">-Plats</span><span class="sxs-lookup"><span data-stu-id="99195-111">-Location</span></span>
<span data-ttu-id="99195-112">Anger namnet på den geografiska platsen för valvet.</span><span class="sxs-lookup"><span data-stu-id="99195-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99195-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="99195-113">-Name</span></span>
<span data-ttu-id="99195-114">Anger namnet på det valv som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="99195-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99195-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99195-115">-ResourceGroupName</span></span>
<span data-ttu-id="99195-116">Anger namnet på den Azure-adressresurs som du vill skapa eller från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="99195-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99195-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99195-117">-Confirm</span></span>
<span data-ttu-id="99195-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99195-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99195-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99195-119">-WhatIf</span></span>
<span data-ttu-id="99195-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99195-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99195-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99195-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99195-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99195-122">-DefaultProfile</span></span>
<span data-ttu-id="99195-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99195-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99195-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99195-124">CommonParameters</span></span>
<span data-ttu-id="99195-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99195-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99195-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99195-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99195-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99195-127">INPUTS</span></span>

### <span data-ttu-id="99195-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="99195-128">None</span></span>

## <span data-ttu-id="99195-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99195-129">OUTPUTS</span></span>

### <span data-ttu-id="99195-130">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="99195-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="99195-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99195-131">NOTES</span></span>

## <span data-ttu-id="99195-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99195-132">RELATED LINKS</span></span>

[<span data-ttu-id="99195-133">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="99195-133">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="99195-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="99195-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="99195-135">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="99195-135">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)

