---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 9f594b61b1ad34a39ea0a84381f6181cadc418c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755915"
---
# <span data-ttu-id="dd503-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="dd503-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="dd503-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd503-102">SYNOPSIS</span></span>
<span data-ttu-id="dd503-103">Hämtar information om virtuella datorer som hanteras av webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="dd503-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd503-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd503-104">SYNTAX</span></span>

### <span data-ttu-id="dd503-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="dd503-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd503-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="dd503-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd503-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="dd503-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd503-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd503-108">DESCRIPTION</span></span>
<span data-ttu-id="dd503-109">Cmdleten **Get-AzureRmSiteRecoveryVM** hämtar information om virtuella datorer som hanteras i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="dd503-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="dd503-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd503-110">EXAMPLES</span></span>

## <span data-ttu-id="dd503-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd503-111">PARAMETERS</span></span>

### <span data-ttu-id="dd503-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="dd503-112">-FriendlyName</span></span>
<span data-ttu-id="dd503-113">Anger det egna namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dd503-113">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd503-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="dd503-114">-Name</span></span>
<span data-ttu-id="dd503-115">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="dd503-115">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd503-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dd503-116">-ProtectionContainer</span></span>
<span data-ttu-id="dd503-117">Anger objekt för objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="dd503-117">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd503-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd503-118">-DefaultProfile</span></span>
<span data-ttu-id="dd503-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd503-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd503-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd503-120">CommonParameters</span></span>
<span data-ttu-id="dd503-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd503-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd503-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd503-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd503-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd503-123">INPUTS</span></span>

### <span data-ttu-id="dd503-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dd503-124">ASRProtectionContainer</span></span>
<span data-ttu-id="dd503-125">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="dd503-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="dd503-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="dd503-126">ASRProtectionContainer</span></span>
<span data-ttu-id="dd503-127">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="dd503-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="dd503-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd503-128">OUTPUTS</span></span>

### <span data-ttu-id="dd503-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="dd503-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="dd503-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd503-130">NOTES</span></span>

## <span data-ttu-id="dd503-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd503-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd503-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="dd503-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
