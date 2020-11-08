---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099586"
---
# <span data-ttu-id="30227-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="30227-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="30227-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30227-102">SYNOPSIS</span></span>
<span data-ttu-id="30227-103">Hämtar ett certifikat objekt från en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="30227-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="30227-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30227-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="30227-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30227-105">DESCRIPTION</span></span>
<span data-ttu-id="30227-106">Cmdleten **Get-AzureCertificate** hämtar ett certifikat objekt från en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="30227-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="30227-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30227-107">EXAMPLES</span></span>

### <span data-ttu-id="30227-108">Exempel 1: skaffa certifikat från en tjänst</span><span class="sxs-lookup"><span data-stu-id="30227-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="30227-109">Det här kommandot hämtar certifikat objekt från tjänsten som heter ContosoService och lagrar dem sedan i $AzureCert variabel.</span><span class="sxs-lookup"><span data-stu-id="30227-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="30227-110">Exempel 2: skaffa ett certifikat från en tjänst</span><span class="sxs-lookup"><span data-stu-id="30227-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="30227-111">Det här kommandot hämtar certifikatet som identifieras av angivet tumavtryck från den tjänst som heter ContosoService och lagrar det sedan i $AzureCert variabel.</span><span class="sxs-lookup"><span data-stu-id="30227-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="30227-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30227-112">PARAMETERS</span></span>

### <span data-ttu-id="30227-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="30227-113">-InformationAction</span></span>
<span data-ttu-id="30227-114">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="30227-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="30227-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="30227-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="30227-116">Vidare</span><span class="sxs-lookup"><span data-stu-id="30227-116">Continue</span></span>
- <span data-ttu-id="30227-117">Över</span><span class="sxs-lookup"><span data-stu-id="30227-117">Ignore</span></span>
- <span data-ttu-id="30227-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="30227-118">Inquire</span></span>
- <span data-ttu-id="30227-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="30227-119">SilentlyContinue</span></span>
- <span data-ttu-id="30227-120">Stanna</span><span class="sxs-lookup"><span data-stu-id="30227-120">Stop</span></span>
- <span data-ttu-id="30227-121">Avbryt</span><span class="sxs-lookup"><span data-stu-id="30227-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30227-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="30227-122">-InformationVariable</span></span>
<span data-ttu-id="30227-123">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="30227-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30227-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="30227-124">-Profile</span></span>
<span data-ttu-id="30227-125">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="30227-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30227-126">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="30227-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30227-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="30227-127">-ServiceName</span></span>
<span data-ttu-id="30227-128">Anger namnet på den Azure-tjänst som den här cmdleten får ett certifikat från.</span><span class="sxs-lookup"><span data-stu-id="30227-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30227-129">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="30227-129">-Thumbprint</span></span>
<span data-ttu-id="30227-130">Anger tumavtrycket för det certifikat som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="30227-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30227-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="30227-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="30227-132">Anger den algoritm som används för att skapa certifikatutfärdarcertifikatet.</span><span class="sxs-lookup"><span data-stu-id="30227-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30227-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30227-133">CommonParameters</span></span>
<span data-ttu-id="30227-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30227-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30227-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30227-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30227-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30227-136">INPUTS</span></span>

## <span data-ttu-id="30227-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30227-137">OUTPUTS</span></span>

### <span data-ttu-id="30227-138">CertificateContext</span><span class="sxs-lookup"><span data-stu-id="30227-138">CertificateContext</span></span>

## <span data-ttu-id="30227-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30227-139">NOTES</span></span>

## <span data-ttu-id="30227-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30227-140">RELATED LINKS</span></span>

[<span data-ttu-id="30227-141">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="30227-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="30227-142">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="30227-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="30227-143">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="30227-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


