---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 9547a3f3aed86bd7458f9fbf1f1a4375e2d95086
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089809"
---
# <span data-ttu-id="aa1ed-101">Set-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aa1ed-101">Set-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="aa1ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa1ed-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1ed-103">Anger autentiseringsuppgifter för lagrings kontot för en enhet.</span><span class="sxs-lookup"><span data-stu-id="aa1ed-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="aa1ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa1ed-104">SYNTAX</span></span>

### <span data-ttu-id="aa1ed-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="aa1ed-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa1ed-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa1ed-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa1ed-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa1ed-107">SetByParentObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSDataBoxEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa1ed-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa1ed-108">DESCRIPTION</span></span>
<span data-ttu-id="aa1ed-109">Cmdleten **set-AzDataBoxEdgeStorageAccountCredential** uppdaterar lagrings konto autentiseringsuppgiften som motsvarar ett lagrings konto i data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="aa1ed-109">The **Set-AzDataBoxEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Data Box Edge device.</span></span>

## <span data-ttu-id="aa1ed-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa1ed-110">EXAMPLES</span></span>

### <span data-ttu-id="aa1ed-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aa1ed-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="aa1ed-112">Hjälper till att rotera snabb tangenter för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="aa1ed-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="aa1ed-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa1ed-113">PARAMETERS</span></span>

### <span data-ttu-id="aa1ed-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa1ed-114">-AsJob</span></span>
<span data-ttu-id="aa1ed-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="aa1ed-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa1ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1ed-116">-DefaultProfile</span></span>
<span data-ttu-id="aa1ed-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aa1ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa1ed-118">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="aa1ed-118">-DeviceName</span></span>
<span data-ttu-id="aa1ed-119">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="aa1ed-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ed-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aa1ed-120">-EncryptionKey</span></span>
<span data-ttu-id="aa1ed-121">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="aa1ed-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ed-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa1ed-122">-InputObject</span></span>
<span data-ttu-id="aa1ed-123">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="aa1ed-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ed-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa1ed-124">-Name</span></span>
<span data-ttu-id="aa1ed-125">Namn på det lagrings konto som ska användas</span><span class="sxs-lookup"><span data-stu-id="aa1ed-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ed-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa1ed-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa1ed-127">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="aa1ed-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ed-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa1ed-128">-ResourceId</span></span>
<span data-ttu-id="aa1ed-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa1ed-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ed-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="aa1ed-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="aa1ed-131">Ange åtkomst nycklar för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="aa1ed-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa1ed-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aa1ed-132">-Confirm</span></span>
<span data-ttu-id="aa1ed-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aa1ed-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa1ed-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa1ed-134">-WhatIf</span></span>
<span data-ttu-id="aa1ed-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aa1ed-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa1ed-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aa1ed-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa1ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1ed-137">CommonParameters</span></span>
<span data-ttu-id="aa1ed-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa1ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1ed-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa1ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1ed-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa1ed-140">INPUTS</span></span>

### <span data-ttu-id="aa1ed-141">System. String</span><span class="sxs-lookup"><span data-stu-id="aa1ed-141">System.String</span></span>

### <span data-ttu-id="aa1ed-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aa1ed-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="aa1ed-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa1ed-143">OUTPUTS</span></span>

### <span data-ttu-id="aa1ed-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aa1ed-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="aa1ed-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa1ed-145">NOTES</span></span>

## <span data-ttu-id="aa1ed-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa1ed-146">RELATED LINKS</span></span>
