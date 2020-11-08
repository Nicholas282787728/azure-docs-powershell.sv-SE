---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099397"
---
# <span data-ttu-id="ac185-101">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="ac185-101">Remove-AzureCertificate</span></span>

## <span data-ttu-id="ac185-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac185-102">SYNOPSIS</span></span>
<span data-ttu-id="ac185-103">Tar bort ett certifikat från en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="ac185-103">Removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="ac185-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac185-104">SYNTAX</span></span>

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac185-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac185-105">DESCRIPTION</span></span>
<span data-ttu-id="ac185-106">Cmdleten **Remove-AzureCertificate** tar bort ett certifikat från en Azure-tjänst.</span><span class="sxs-lookup"><span data-stu-id="ac185-106">The **Remove-AzureCertificate** cmdlet removes a certificate from an Azure service.</span></span>

## <span data-ttu-id="ac185-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac185-107">EXAMPLES</span></span>

### <span data-ttu-id="ac185-108">Exempel 1: ta bort ett certifikat från en tjänst</span><span class="sxs-lookup"><span data-stu-id="ac185-108">Example 1: Remove a certificate from a service</span></span>
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="ac185-109">Det här kommandot tar bort det certifikat objekt som har det angivna tumavtrycket från moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ac185-109">This command removes the certificate object that has the specified thumbprint from the cloud service.</span></span>

### <span data-ttu-id="ac185-110">Exempel 2: ta bort alla certifikat från en tjänst</span><span class="sxs-lookup"><span data-stu-id="ac185-110">Example 2: Remove all certificates from a service</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

<span data-ttu-id="ac185-111">Det här kommandot får alla certifikat från tjänsten som heter ContosoService med hjälp av cmdleten **Get-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="ac185-111">This command gets all the certificates from the service named ContosoService by using the **Get-AzureCertificate** cmdlet.</span></span>
<span data-ttu-id="ac185-112">Kommandot skickar varje certifikat till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ac185-112">The command passes each certificate to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ac185-113">Denna cmdlet tar bort varje certifikat från moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ac185-113">That cmdlet removes each certificate from the cloud service.</span></span>

### <span data-ttu-id="ac185-114">Exempel 3: ta bort alla certifikat från en tjänst som använder en viss tumavtryck</span><span class="sxs-lookup"><span data-stu-id="ac185-114">Example 3: Remove all certificates from a service that use a specific thumbprint algorithm</span></span>
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

<span data-ttu-id="ac185-115">Det här kommandot får alla certifikat från tjänsten som heter ContosoService och som använder SHA1-tumavtrycket.</span><span class="sxs-lookup"><span data-stu-id="ac185-115">This command gets all the certificates from the service named ContosoService that use the sha1 thumbprint algorithm.</span></span>
<span data-ttu-id="ac185-116">Kommandot skickar varje certifikat till den aktuella cmdleten, vilket innebär att varje certifikat tas bort.</span><span class="sxs-lookup"><span data-stu-id="ac185-116">The command passes each certificate to the current cmdlet, which removes each certificate.</span></span>

## <span data-ttu-id="ac185-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac185-117">PARAMETERS</span></span>

### <span data-ttu-id="ac185-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ac185-118">-InformationAction</span></span>
<span data-ttu-id="ac185-119">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="ac185-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ac185-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="ac185-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac185-121">Vidare</span><span class="sxs-lookup"><span data-stu-id="ac185-121">Continue</span></span>
- <span data-ttu-id="ac185-122">Över</span><span class="sxs-lookup"><span data-stu-id="ac185-122">Ignore</span></span>
- <span data-ttu-id="ac185-123">Inquire</span><span class="sxs-lookup"><span data-stu-id="ac185-123">Inquire</span></span>
- <span data-ttu-id="ac185-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ac185-124">SilentlyContinue</span></span>
- <span data-ttu-id="ac185-125">Stanna</span><span class="sxs-lookup"><span data-stu-id="ac185-125">Stop</span></span>
- <span data-ttu-id="ac185-126">Avbryt</span><span class="sxs-lookup"><span data-stu-id="ac185-126">Suspend</span></span>

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

### <span data-ttu-id="ac185-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ac185-127">-InformationVariable</span></span>
<span data-ttu-id="ac185-128">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="ac185-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ac185-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="ac185-129">-Profile</span></span>
<span data-ttu-id="ac185-130">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="ac185-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ac185-131">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="ac185-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ac185-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ac185-132">-ServiceName</span></span>
<span data-ttu-id="ac185-133">Anger namnet på den Azure-tjänst som den här cmdleten tar bort ett certifikat från.</span><span class="sxs-lookup"><span data-stu-id="ac185-133">Specifies the name of the Azure service from which this cmdlet removes a certificate.</span></span>

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

### <span data-ttu-id="ac185-134">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="ac185-134">-Thumbprint</span></span>
<span data-ttu-id="ac185-135">Anger tumavtrycket för det certifikat som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="ac185-135">Specifies the thumbprint of the certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac185-136">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ac185-136">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ac185-137">Anger den algoritm som används för att skapa certifikatutfärdarcertifikatet.</span><span class="sxs-lookup"><span data-stu-id="ac185-137">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac185-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac185-138">CommonParameters</span></span>
<span data-ttu-id="ac185-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac185-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac185-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac185-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac185-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac185-141">INPUTS</span></span>

## <span data-ttu-id="ac185-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac185-142">OUTPUTS</span></span>

### <span data-ttu-id="ac185-143">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="ac185-143">ManagementOperationContext</span></span>

## <span data-ttu-id="ac185-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac185-144">NOTES</span></span>

## <span data-ttu-id="ac185-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac185-145">RELATED LINKS</span></span>

[<span data-ttu-id="ac185-146">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="ac185-146">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="ac185-147">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="ac185-147">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="ac185-148">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="ac185-148">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)


