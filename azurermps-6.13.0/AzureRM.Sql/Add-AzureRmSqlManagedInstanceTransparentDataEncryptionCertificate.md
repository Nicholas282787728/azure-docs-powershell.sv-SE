---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: 9fe8e36a752b4643ba44a59e8c44954bf25284c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755808"
---
# <span data-ttu-id="300cf-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="300cf-101">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="300cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="300cf-102">SYNOPSIS</span></span>
<span data-ttu-id="300cf-103">Lägger till ett transparent data krypterings certifikat för den angivna hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="300cf-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="300cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="300cf-104">SYNTAX</span></span>

```
Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="300cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="300cf-105">DESCRIPTION</span></span>
<span data-ttu-id="300cf-106">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate lägger till ett transparent data krypterings certifikat för den angivna hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="300cf-106">The Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="300cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="300cf-107">EXAMPLES</span></span>

### <span data-ttu-id="300cf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="300cf-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="300cf-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="300cf-109">PARAMETERS</span></span>

### <span data-ttu-id="300cf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="300cf-110">-DefaultProfile</span></span>
<span data-ttu-id="300cf-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="300cf-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="300cf-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="300cf-112">-ManagedInstanceName</span></span>
<span data-ttu-id="300cf-113">Namnet på den hanterade förekomsten</span><span class="sxs-lookup"><span data-stu-id="300cf-113">The managed instance name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300cf-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="300cf-114">-PassThru</span></span>
<span data-ttu-id="300cf-115">Vid lyckad körning returneras ett certifikat objekt som har lagts till.</span><span class="sxs-lookup"><span data-stu-id="300cf-115">On Successful execution, returns certificate object that was added.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300cf-116">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="300cf-116">-Password</span></span>
<span data-ttu-id="300cf-117">Lösen ordet för ett transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="300cf-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300cf-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="300cf-118">-PrivateBlob</span></span>
<span data-ttu-id="300cf-119">Den privata blobben för transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="300cf-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="300cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="300cf-121">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="300cf-121">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="300cf-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="300cf-122">-Confirm</span></span>
<span data-ttu-id="300cf-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="300cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="300cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="300cf-124">-WhatIf</span></span>
<span data-ttu-id="300cf-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="300cf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="300cf-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="300cf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="300cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="300cf-127">CommonParameters</span></span>
<span data-ttu-id="300cf-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="300cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="300cf-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="300cf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="300cf-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="300cf-130">INPUTS</span></span>

### <span data-ttu-id="300cf-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="300cf-131">None</span></span>

## <span data-ttu-id="300cf-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="300cf-132">OUTPUTS</span></span>

### <span data-ttu-id="300cf-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="300cf-133">System.Boolean</span></span>

## <span data-ttu-id="300cf-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="300cf-134">NOTES</span></span>

## <span data-ttu-id="300cf-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="300cf-135">RELATED LINKS</span></span>
