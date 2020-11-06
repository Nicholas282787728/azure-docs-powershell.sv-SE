---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: A5697F1E-623A-4E26-96C8-6197852BFFAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVM.md
ms.openlocfilehash: 1cdcbad6af048d7fc462dbe8a28fdd02fd576aa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582968"
---
# <span data-ttu-id="3935f-101">Get-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="3935f-101">Get-AzureRmSiteRecoveryVM</span></span>

## <span data-ttu-id="3935f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3935f-102">SYNOPSIS</span></span>
<span data-ttu-id="3935f-103">Hämtar information om virtuella datorer som hanteras av webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="3935f-103">Gets information about Site Recovery-managed virtual machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3935f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3935f-104">SYNTAX</span></span>

### <span data-ttu-id="3935f-105">ByObject (standard)</span><span class="sxs-lookup"><span data-stu-id="3935f-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryVM -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3935f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="3935f-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryVM -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3935f-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3935f-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryVM -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3935f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3935f-108">DESCRIPTION</span></span>
<span data-ttu-id="3935f-109">Cmdleten **Get-AzureRmSiteRecoveryVM** hämtar information om virtuella datorer som hanteras i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3935f-109">The **Get-AzureRmSiteRecoveryVM** cmdlet gets information about virtual machines managed in Azure Site Recovery.</span></span>

## <span data-ttu-id="3935f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3935f-110">EXAMPLES</span></span>

## <span data-ttu-id="3935f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3935f-111">PARAMETERS</span></span>

### <span data-ttu-id="3935f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3935f-112">-DefaultProfile</span></span>
<span data-ttu-id="3935f-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3935f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3935f-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="3935f-114">-FriendlyName</span></span>
<span data-ttu-id="3935f-115">Anger det egna namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3935f-115">Specifies the friendly name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3935f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="3935f-116">-Name</span></span>
<span data-ttu-id="3935f-117">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="3935f-117">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3935f-118">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3935f-118">-ProtectionContainer</span></span>
<span data-ttu-id="3935f-119">Anger objekt för objektet för webbplats återställnings skydd.</span><span class="sxs-lookup"><span data-stu-id="3935f-119">Specifies the Site Recovery protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3935f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3935f-120">CommonParameters</span></span>
<span data-ttu-id="3935f-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3935f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3935f-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3935f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3935f-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3935f-123">INPUTS</span></span>

### <span data-ttu-id="3935f-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3935f-124">ASRProtectionContainer</span></span>
<span data-ttu-id="3935f-125">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3935f-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

### <span data-ttu-id="3935f-126">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3935f-126">ASRProtectionContainer</span></span>
<span data-ttu-id="3935f-127">Parametern ' ProtectionContainer ' godkänner värdet av typen ' ASRProtectionContainer ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3935f-127">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="3935f-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3935f-128">OUTPUTS</span></span>

### <span data-ttu-id="3935f-129">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVirtualMachine]</span><span class="sxs-lookup"><span data-stu-id="3935f-129">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVirtualMachine]</span></span>

## <span data-ttu-id="3935f-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3935f-130">NOTES</span></span>

## <span data-ttu-id="3935f-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3935f-131">RELATED LINKS</span></span>

[<span data-ttu-id="3935f-132">Set-AzureRmSiteRecoveryVM</span><span class="sxs-lookup"><span data-stu-id="3935f-132">Set-AzureRmSiteRecoveryVM</span></span>](./Set-AzureRmSiteRecoveryVM.md)
