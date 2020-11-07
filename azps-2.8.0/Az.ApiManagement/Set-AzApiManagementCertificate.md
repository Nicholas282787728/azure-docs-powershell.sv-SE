---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 1eab0b6f9f80a4fb921a64966c758cdaa08c51df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745668"
---
# <span data-ttu-id="3db79-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3db79-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="3db79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3db79-102">SYNOPSIS</span></span>
<span data-ttu-id="3db79-103">Ändrar ett API-Management-certifikat som är konfigurerat för ömsesidig autentisering med Server delen.</span><span class="sxs-lookup"><span data-stu-id="3db79-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="3db79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3db79-104">SYNTAX</span></span>

### <span data-ttu-id="3db79-105">LoadFromFile (standard)</span><span class="sxs-lookup"><span data-stu-id="3db79-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3db79-106">RAW</span><span class="sxs-lookup"><span data-stu-id="3db79-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3db79-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3db79-107">DESCRIPTION</span></span>
<span data-ttu-id="3db79-108">Cmdleten **set-AzApiManagementCertificate** ändrar ett certifikat för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="3db79-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="3db79-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3db79-109">EXAMPLES</span></span>

### <span data-ttu-id="3db79-110">Exempel 1: ändra ett certifikat</span><span class="sxs-lookup"><span data-stu-id="3db79-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="3db79-111">Det här kommandot ändrar angivet API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="3db79-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="3db79-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3db79-112">PARAMETERS</span></span>

### <span data-ttu-id="3db79-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="3db79-113">-CertificateId</span></span>
<span data-ttu-id="3db79-114">Anger ID för det certifikat som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="3db79-114">Specifies the ID of the certificate to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3db79-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3db79-115">-Context</span></span>
<span data-ttu-id="3db79-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3db79-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3db79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db79-117">-DefaultProfile</span></span>
<span data-ttu-id="3db79-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3db79-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3db79-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3db79-119">-PassThru</span></span>
<span data-ttu-id="3db79-120">passthru</span><span class="sxs-lookup"><span data-stu-id="3db79-120">passthru</span></span>

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

### <span data-ttu-id="3db79-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="3db79-121">-PfxBytes</span></span>
<span data-ttu-id="3db79-122">Anger en matris med byte för certifikat filen i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="3db79-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="3db79-123">Den här parametern är obligatorisk om du inte anger parametern *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="3db79-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3db79-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="3db79-124">-PfxFilePath</span></span>
<span data-ttu-id="3db79-125">Anger sökvägen till certifikat filen i PFX-format för att skapa och ladda upp.</span><span class="sxs-lookup"><span data-stu-id="3db79-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="3db79-126">Den här parametern är obligatorisk om du inte anger parametern *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="3db79-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3db79-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="3db79-127">-PfxPassword</span></span>
<span data-ttu-id="3db79-128">Anger lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="3db79-128">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3db79-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db79-129">CommonParameters</span></span>
<span data-ttu-id="3db79-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db79-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db79-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3db79-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db79-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3db79-132">INPUTS</span></span>

### <span data-ttu-id="3db79-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3db79-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3db79-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3db79-134">System.String</span></span>

### <span data-ttu-id="3db79-135">System. byte []</span><span class="sxs-lookup"><span data-stu-id="3db79-135">System.Byte[]</span></span>

### <span data-ttu-id="3db79-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3db79-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3db79-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3db79-137">OUTPUTS</span></span>

### <span data-ttu-id="3db79-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3db79-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="3db79-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3db79-139">NOTES</span></span>

## <span data-ttu-id="3db79-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3db79-140">RELATED LINKS</span></span>

[<span data-ttu-id="3db79-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3db79-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="3db79-142">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3db79-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="3db79-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3db79-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


