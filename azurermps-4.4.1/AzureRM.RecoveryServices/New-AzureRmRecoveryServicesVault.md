---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574550"
---
# <span data-ttu-id="faac8-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="faac8-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="faac8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="faac8-102">SYNOPSIS</span></span>
<span data-ttu-id="faac8-103">Skapar ett nytt Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="faac8-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faac8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="faac8-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faac8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="faac8-105">DESCRIPTION</span></span>
<span data-ttu-id="faac8-106">Cmdleten **New-AzureRmRecoveryServicesVault** skapar ett nytt Recovery Services-valv.</span><span class="sxs-lookup"><span data-stu-id="faac8-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="faac8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="faac8-107">EXAMPLES</span></span>

## <span data-ttu-id="faac8-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="faac8-108">PARAMETERS</span></span>

### <span data-ttu-id="faac8-109">-Plats</span><span class="sxs-lookup"><span data-stu-id="faac8-109">-Location</span></span>
<span data-ttu-id="faac8-110">Anger namnet på den geografiska platsen för valvet.</span><span class="sxs-lookup"><span data-stu-id="faac8-110">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faac8-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="faac8-111">-Name</span></span>
<span data-ttu-id="faac8-112">Anger namnet på det valv som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="faac8-112">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faac8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faac8-113">-ResourceGroupName</span></span>
<span data-ttu-id="faac8-114">Anger namnet på den Azure-adressresurs som du vill skapa eller från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="faac8-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faac8-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="faac8-115">-Confirm</span></span>
<span data-ttu-id="faac8-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="faac8-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faac8-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faac8-117">-WhatIf</span></span>
<span data-ttu-id="faac8-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="faac8-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faac8-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="faac8-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faac8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faac8-120">-DefaultProfile</span></span>
<span data-ttu-id="faac8-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="faac8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faac8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faac8-122">CommonParameters</span></span>
<span data-ttu-id="faac8-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faac8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faac8-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faac8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faac8-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="faac8-125">INPUTS</span></span>

## <span data-ttu-id="faac8-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="faac8-126">OUTPUTS</span></span>

### <span data-ttu-id="faac8-127">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="faac8-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="faac8-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="faac8-128">NOTES</span></span>

## <span data-ttu-id="faac8-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="faac8-129">RELATED LINKS</span></span>

[<span data-ttu-id="faac8-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="faac8-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="faac8-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="faac8-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="faac8-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="faac8-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


