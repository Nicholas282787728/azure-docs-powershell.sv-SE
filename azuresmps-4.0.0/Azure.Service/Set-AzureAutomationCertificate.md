---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099658"
---
# <span data-ttu-id="67b7f-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="67b7f-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="67b7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67b7f-102">SYNOPSIS</span></span>

<span data-ttu-id="67b7f-103">Ändrar konfigurationen för ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="67b7f-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="67b7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67b7f-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="67b7f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67b7f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="67b7f-106">Cmdleten **set-AzureAutomationCertificate** ändrar konfigurationen för ett certifikat i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="67b7f-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="67b7f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67b7f-107">EXAMPLES</span></span>

### <span data-ttu-id="67b7f-108">Exempel 1: uppdatera ett certifikat</span><span class="sxs-lookup"><span data-stu-id="67b7f-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="67b7f-109">Dessa kommandon uppdaterar ett befintligt certifikat som heter mina certifikat i Automation.</span><span class="sxs-lookup"><span data-stu-id="67b7f-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="67b7f-110">Det första kommandot skapar lösen ordet för den certifikat fil som används i det andra kommandot som uppdaterar certifikatet.</span><span class="sxs-lookup"><span data-stu-id="67b7f-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="67b7f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67b7f-111">PARAMETERS</span></span>

### <span data-ttu-id="67b7f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67b7f-112">-AutomationAccountName</span></span>
<span data-ttu-id="67b7f-113">Anger namnet på Automation-kontot med certifikatet.</span><span class="sxs-lookup"><span data-stu-id="67b7f-113">Specifies the name of the Automation account with the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b7f-114">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="67b7f-114">-Description</span></span>
<span data-ttu-id="67b7f-115">Anger en beskrivning av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="67b7f-115">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="67b7f-116">– Kan exporteras</span><span class="sxs-lookup"><span data-stu-id="67b7f-116">-Exportable</span></span>
<span data-ttu-id="67b7f-117">Anger att certifikatet kan exporteras.</span><span class="sxs-lookup"><span data-stu-id="67b7f-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b7f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="67b7f-118">-Name</span></span>
<span data-ttu-id="67b7f-119">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="67b7f-119">Specifies the name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b7f-120">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="67b7f-120">-Password</span></span>
<span data-ttu-id="67b7f-121">Anger lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="67b7f-121">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b7f-122">-Path</span><span class="sxs-lookup"><span data-stu-id="67b7f-122">-Path</span></span>
<span data-ttu-id="67b7f-123">Anger sökvägen till en skript fil som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="67b7f-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="67b7f-124">Filen kan vara. cer eller. pfx.</span><span class="sxs-lookup"><span data-stu-id="67b7f-124">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="67b7f-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="67b7f-125">-Profile</span></span>
<span data-ttu-id="67b7f-126">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="67b7f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="67b7f-127">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="67b7f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="67b7f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b7f-128">CommonParameters</span></span>
<span data-ttu-id="67b7f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b7f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b7f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b7f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b7f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67b7f-131">INPUTS</span></span>

## <span data-ttu-id="67b7f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67b7f-132">OUTPUTS</span></span>

### <span data-ttu-id="67b7f-133">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="67b7f-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="67b7f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67b7f-134">NOTES</span></span>

## <span data-ttu-id="67b7f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67b7f-135">RELATED LINKS</span></span>

[<span data-ttu-id="67b7f-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="67b7f-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="67b7f-137">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="67b7f-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="67b7f-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="67b7f-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


