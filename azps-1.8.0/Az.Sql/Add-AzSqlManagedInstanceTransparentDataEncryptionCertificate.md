---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: dc73939aaae76c0444307cbd1aa6bfb08711b2e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746809"
---
# <span data-ttu-id="16684-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="16684-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="16684-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16684-102">SYNOPSIS</span></span>
<span data-ttu-id="16684-103">Lägger till ett transparent data krypterings certifikat för den angivna hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="16684-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="16684-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16684-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16684-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16684-105">DESCRIPTION</span></span>
<span data-ttu-id="16684-106">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate lägger till ett transparent data krypterings certifikat för den angivna hanterade instansen</span><span class="sxs-lookup"><span data-stu-id="16684-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="16684-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16684-107">EXAMPLES</span></span>

### <span data-ttu-id="16684-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="16684-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="16684-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16684-109">PARAMETERS</span></span>

### <span data-ttu-id="16684-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16684-110">-DefaultProfile</span></span>
<span data-ttu-id="16684-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="16684-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16684-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="16684-112">-ManagedInstanceName</span></span>
<span data-ttu-id="16684-113">Namnet på den hanterade förekomsten</span><span class="sxs-lookup"><span data-stu-id="16684-113">The managed instance name</span></span>

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

### <span data-ttu-id="16684-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16684-114">-PassThru</span></span>
<span data-ttu-id="16684-115">Vid lyckad körning returneras ett certifikat objekt som har lagts till.</span><span class="sxs-lookup"><span data-stu-id="16684-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="16684-116">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="16684-116">-Password</span></span>
<span data-ttu-id="16684-117">Lösen ordet för ett transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="16684-117">The Password for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="16684-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="16684-118">-PrivateBlob</span></span>
<span data-ttu-id="16684-119">Den privata blobben för transparent data krypterings certifikat</span><span class="sxs-lookup"><span data-stu-id="16684-119">The Private blob for Transparent Data Encryption Certificate</span></span>

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

### <span data-ttu-id="16684-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16684-120">-ResourceGroupName</span></span>
<span data-ttu-id="16684-121">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="16684-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="16684-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16684-122">-Confirm</span></span>
<span data-ttu-id="16684-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16684-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16684-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16684-124">-WhatIf</span></span>
<span data-ttu-id="16684-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16684-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16684-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16684-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16684-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16684-127">CommonParameters</span></span>
<span data-ttu-id="16684-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16684-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16684-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16684-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16684-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16684-130">INPUTS</span></span>

### <span data-ttu-id="16684-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="16684-131">None</span></span>

## <span data-ttu-id="16684-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16684-132">OUTPUTS</span></span>

### <span data-ttu-id="16684-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="16684-133">System.Boolean</span></span>

## <span data-ttu-id="16684-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16684-134">NOTES</span></span>

## <span data-ttu-id="16684-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16684-135">RELATED LINKS</span></span>