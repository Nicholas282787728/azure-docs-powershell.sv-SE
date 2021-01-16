---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419667"
---
# <span data-ttu-id="8601a-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8601a-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="8601a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8601a-102">SYNOPSIS</span></span>
<span data-ttu-id="8601a-103">Lägger till ett transparent data krypterings certifikat för den angivna hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="8601a-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="8601a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8601a-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8601a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8601a-105">DESCRIPTION</span></span>
<span data-ttu-id="8601a-106">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate lägger till ett transparent data krypterings certifikat för den angivna hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="8601a-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="8601a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8601a-107">EXAMPLES</span></span>

### <span data-ttu-id="8601a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8601a-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="8601a-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8601a-109">PARAMETERS</span></span>

### <span data-ttu-id="8601a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8601a-110">-DefaultProfile</span></span>
<span data-ttu-id="8601a-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8601a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8601a-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="8601a-112">-ManagedInstanceName</span></span>
<span data-ttu-id="8601a-113">Namnet på den hanterade förekomsten</span><span class="sxs-lookup"><span data-stu-id="8601a-113">The managed instance name</span></span>

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

### <span data-ttu-id="8601a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8601a-114">-PassThru</span></span>
<span data-ttu-id="8601a-115">Vid lyckad körning returneras ett certifikat objekt som har lagts till.</span><span class="sxs-lookup"><span data-stu-id="8601a-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="8601a-116">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="8601a-116">-Password</span></span>
<span data-ttu-id="8601a-117">Lösen ordet för ett transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="8601a-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="8601a-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="8601a-118">-PrivateBlob</span></span>
<span data-ttu-id="8601a-119">Den privata blobben för transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="8601a-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="8601a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8601a-120">-ResourceGroupName</span></span>
<span data-ttu-id="8601a-121">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="8601a-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="8601a-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8601a-122">-Confirm</span></span>
<span data-ttu-id="8601a-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8601a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8601a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8601a-124">-WhatIf</span></span>
<span data-ttu-id="8601a-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8601a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8601a-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8601a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8601a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8601a-127">CommonParameters</span></span>
<span data-ttu-id="8601a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8601a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8601a-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8601a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8601a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8601a-130">INPUTS</span></span>

### <span data-ttu-id="8601a-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="8601a-131">None</span></span>

## <span data-ttu-id="8601a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8601a-132">OUTPUTS</span></span>

### <span data-ttu-id="8601a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8601a-133">System.Boolean</span></span>

## <span data-ttu-id="8601a-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8601a-134">NOTES</span></span>

## <span data-ttu-id="8601a-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8601a-135">RELATED LINKS</span></span>
