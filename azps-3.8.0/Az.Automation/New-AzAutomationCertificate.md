---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092700"
---
# <span data-ttu-id="a60f8-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a60f8-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="a60f8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a60f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a60f8-103">Skapar ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="a60f8-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="a60f8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a60f8-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a60f8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a60f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a60f8-106">Cmdleten **New-AzAutomationCertificate** skapar ett certifikat i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a60f8-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="a60f8-107">Ange sökvägen till en certifikat fil som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="a60f8-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="a60f8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a60f8-108">EXAMPLES</span></span>

### <span data-ttu-id="a60f8-109">Exempel 1: skapa ett nytt certifikat</span><span class="sxs-lookup"><span data-stu-id="a60f8-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a60f8-110">Med det första kommandot konverteras ett oformaterat lösen ord till en säker sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60f8-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="a60f8-111">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="a60f8-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="a60f8-112">Det andra kommandot skapar ett certifikat som heter ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="a60f8-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="a60f8-113">Kommandot använder det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="a60f8-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="a60f8-114">Kommandot anger konto namnet och sökvägen till filen som laddas upp.</span><span class="sxs-lookup"><span data-stu-id="a60f8-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="a60f8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a60f8-115">PARAMETERS</span></span>

### <span data-ttu-id="a60f8-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a60f8-116">-AutomationAccountName</span></span>
<span data-ttu-id="a60f8-117">Anger namnet på det Automation-konto som denna cmdlet lagrar certifikatet för.</span><span class="sxs-lookup"><span data-stu-id="a60f8-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60f8-118">-DefaultProfile</span></span>
<span data-ttu-id="a60f8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a60f8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a60f8-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="a60f8-120">-Description</span></span>
<span data-ttu-id="a60f8-121">Anger en beskrivning av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a60f8-121">Specifies a description for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60f8-122">– Kan exporteras</span><span class="sxs-lookup"><span data-stu-id="a60f8-122">-Exportable</span></span>
<span data-ttu-id="a60f8-123">Anger om certifikatet kan exporteras.</span><span class="sxs-lookup"><span data-stu-id="a60f8-123">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60f8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a60f8-124">-Name</span></span>
<span data-ttu-id="a60f8-125">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="a60f8-125">Specifies the name for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60f8-126">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="a60f8-126">-Password</span></span>
<span data-ttu-id="a60f8-127">Anger lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="a60f8-127">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60f8-128">-Path</span><span class="sxs-lookup"><span data-stu-id="a60f8-128">-Path</span></span>
<span data-ttu-id="a60f8-129">Anger sökvägen till en skript fil som denna cmdlet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="a60f8-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="a60f8-130">Filen kan vara en CER-eller en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="a60f8-130">The file can be a .cer or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60f8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60f8-131">-ResourceGroupName</span></span>
<span data-ttu-id="a60f8-132">Anger namnet på den resurs grupp som den här cmdleten skapar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="a60f8-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a60f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60f8-133">CommonParameters</span></span>
<span data-ttu-id="a60f8-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60f8-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a60f8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60f8-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a60f8-136">INPUTS</span></span>

### <span data-ttu-id="a60f8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a60f8-137">System.String</span></span>

### <span data-ttu-id="a60f8-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a60f8-138">System.Security.SecureString</span></span>

### <span data-ttu-id="a60f8-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a60f8-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a60f8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a60f8-140">OUTPUTS</span></span>

### <span data-ttu-id="a60f8-141">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="a60f8-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="a60f8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a60f8-142">NOTES</span></span>

<span data-ttu-id="a60f8-143">Det här kommandot bör köras på en dator som du är administratör för, samt i en upphöjd PowerShell-session; innan certifikatet laddas upp använder denna cmdlet den lokala X. 509-butiken för att hämta tumavtryck och nycklar, och om denna cmdlet körs utanför en upphöjd PowerShell-session visas felet "åtkomst nekad".</span><span class="sxs-lookup"><span data-stu-id="a60f8-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="a60f8-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a60f8-144">RELATED LINKS</span></span>

[<span data-ttu-id="a60f8-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a60f8-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="a60f8-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a60f8-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="a60f8-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a60f8-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


