---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099452"
---
# <span data-ttu-id="b4288-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4288-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="b4288-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4288-102">SYNOPSIS</span></span>

<span data-ttu-id="b4288-103">Skapar ett Azure Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="b4288-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="b4288-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4288-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b4288-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4288-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b4288-106">Cmdleten **New-AzureAutomationCertificate** skapar ett certifikat i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b4288-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="b4288-107">Du anger sökvägen till en certifikat fil som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="b4288-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="b4288-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4288-108">EXAMPLES</span></span>

### <span data-ttu-id="b4288-109">Exempel 1: skapa ett certifikat</span><span class="sxs-lookup"><span data-stu-id="b4288-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="b4288-110">De här kommandona skapar ett certifikat i Azure Automation med namnet mina certifikat.</span><span class="sxs-lookup"><span data-stu-id="b4288-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="b4288-111">Det första kommandot skapar lösen ordet för den certifikat fil som används i det andra kommandot som skapar certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b4288-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="b4288-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4288-112">PARAMETERS</span></span>

### <span data-ttu-id="b4288-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b4288-113">-AutomationAccountName</span></span>
<span data-ttu-id="b4288-114">Anger namnet på det Automation-konto som certifikatet sparas i.</span><span class="sxs-lookup"><span data-stu-id="b4288-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

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

### <span data-ttu-id="b4288-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="b4288-115">-Description</span></span>
<span data-ttu-id="b4288-116">Anger en beskrivning av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b4288-116">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="b4288-117">– Kan exporteras</span><span class="sxs-lookup"><span data-stu-id="b4288-117">-Exportable</span></span>
<span data-ttu-id="b4288-118">Anger att certifikatet kan exporteras.</span><span class="sxs-lookup"><span data-stu-id="b4288-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4288-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4288-119">-Name</span></span>
<span data-ttu-id="b4288-120">Anger ett namn för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b4288-120">Specifies a name for the certificate.</span></span>

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

### <span data-ttu-id="b4288-121">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="b4288-121">-Password</span></span>
<span data-ttu-id="b4288-122">Anger lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="b4288-122">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="b4288-123">-Path</span><span class="sxs-lookup"><span data-stu-id="b4288-123">-Path</span></span>
<span data-ttu-id="b4288-124">Anger sökvägen till en skript fil som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="b4288-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="b4288-125">Filen kan vara. cer eller. pfx.</span><span class="sxs-lookup"><span data-stu-id="b4288-125">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="b4288-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4288-126">-Profile</span></span>
<span data-ttu-id="b4288-127">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b4288-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4288-128">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b4288-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4288-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4288-129">CommonParameters</span></span>
<span data-ttu-id="b4288-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4288-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4288-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4288-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4288-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4288-132">INPUTS</span></span>

## <span data-ttu-id="b4288-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4288-133">OUTPUTS</span></span>

### <span data-ttu-id="b4288-134">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="b4288-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="b4288-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4288-135">NOTES</span></span>

## <span data-ttu-id="b4288-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4288-136">RELATED LINKS</span></span>

[<span data-ttu-id="b4288-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4288-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="b4288-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4288-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="b4288-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b4288-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


