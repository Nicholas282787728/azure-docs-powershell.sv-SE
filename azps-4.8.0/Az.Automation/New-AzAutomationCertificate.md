---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: c80eb16f840fb6d590c139a6ec4b30d73584b741
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101171"
---
# <span data-ttu-id="e0afc-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0afc-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="e0afc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0afc-102">SYNOPSIS</span></span>
<span data-ttu-id="e0afc-103">Skapar ett Automation-certifikat.</span><span class="sxs-lookup"><span data-stu-id="e0afc-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="e0afc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0afc-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0afc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0afc-105">DESCRIPTION</span></span>
<span data-ttu-id="e0afc-106">Cmdleten **New-AzAutomationCertificate** skapar ett certifikat i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e0afc-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="e0afc-107">Ange sökvägen till en certifikat fil som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="e0afc-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="e0afc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0afc-108">EXAMPLES</span></span>

### <span data-ttu-id="e0afc-109">Exempel 1: skapa ett nytt certifikat</span><span class="sxs-lookup"><span data-stu-id="e0afc-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e0afc-110">Med det första kommandot konverteras ett oformaterat lösen ord till en säker sträng med hjälp av ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0afc-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="e0afc-111">Kommandot lagrar objektet i $Password variabel.</span><span class="sxs-lookup"><span data-stu-id="e0afc-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="e0afc-112">Det andra kommandot skapar ett certifikat som heter ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="e0afc-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="e0afc-113">Kommandot använder det lösen ord som lagras i $Password.</span><span class="sxs-lookup"><span data-stu-id="e0afc-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="e0afc-114">Kommandot anger konto namnet och sökvägen till filen som laddas upp.</span><span class="sxs-lookup"><span data-stu-id="e0afc-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="e0afc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0afc-115">PARAMETERS</span></span>

### <span data-ttu-id="e0afc-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e0afc-116">-AutomationAccountName</span></span>
<span data-ttu-id="e0afc-117">Anger namnet på det Automation-konto som denna cmdlet lagrar certifikatet för.</span><span class="sxs-lookup"><span data-stu-id="e0afc-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="e0afc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0afc-118">-DefaultProfile</span></span>
<span data-ttu-id="e0afc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e0afc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0afc-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e0afc-120">-Description</span></span>
<span data-ttu-id="e0afc-121">Anger en beskrivning av certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e0afc-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="e0afc-122">– Kan exporteras</span><span class="sxs-lookup"><span data-stu-id="e0afc-122">-Exportable</span></span>
<span data-ttu-id="e0afc-123">Anger om certifikatet kan exporteras.</span><span class="sxs-lookup"><span data-stu-id="e0afc-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="e0afc-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0afc-124">-Name</span></span>
<span data-ttu-id="e0afc-125">Anger namnet på certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e0afc-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="e0afc-126">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="e0afc-126">-Password</span></span>
<span data-ttu-id="e0afc-127">Anger lösen ordet för certifikat filen.</span><span class="sxs-lookup"><span data-stu-id="e0afc-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="e0afc-128">-Path</span><span class="sxs-lookup"><span data-stu-id="e0afc-128">-Path</span></span>
<span data-ttu-id="e0afc-129">Anger sökvägen till en skript fil som denna cmdlet laddar upp.</span><span class="sxs-lookup"><span data-stu-id="e0afc-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="e0afc-130">Filen kan vara en CER-eller en. pfx-fil.</span><span class="sxs-lookup"><span data-stu-id="e0afc-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="e0afc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0afc-131">-ResourceGroupName</span></span>
<span data-ttu-id="e0afc-132">Anger namnet på den resurs grupp som den här cmdleten skapar ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="e0afc-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="e0afc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0afc-133">CommonParameters</span></span>
<span data-ttu-id="e0afc-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0afc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0afc-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0afc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0afc-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0afc-136">INPUTS</span></span>

### <span data-ttu-id="e0afc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e0afc-137">System.String</span></span>

### <span data-ttu-id="e0afc-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e0afc-138">System.Security.SecureString</span></span>

### <span data-ttu-id="e0afc-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e0afc-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e0afc-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0afc-140">OUTPUTS</span></span>

### <span data-ttu-id="e0afc-141">Microsoft. Azure. commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="e0afc-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="e0afc-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0afc-142">NOTES</span></span>

<span data-ttu-id="e0afc-143">Det här kommandot bör köras på en dator som du är administratör för, samt i en upphöjd PowerShell-session; innan certifikatet laddas upp använder denna cmdlet den lokala X. 509-butiken för att hämta tumavtryck och nycklar, och om denna cmdlet körs utanför en upphöjd PowerShell-session visas felet "åtkomst nekad".</span><span class="sxs-lookup"><span data-stu-id="e0afc-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="e0afc-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0afc-144">RELATED LINKS</span></span>

[<span data-ttu-id="e0afc-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0afc-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="e0afc-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0afc-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="e0afc-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="e0afc-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


