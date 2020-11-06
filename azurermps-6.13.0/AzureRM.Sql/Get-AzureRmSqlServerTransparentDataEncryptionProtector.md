---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 93ab4c51882a4c274fd10727d83f5507c7cfa583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573880"
---
# <span data-ttu-id="e17a9-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="e17a9-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="e17a9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e17a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e17a9-103">Hämtar skyddet för transparent data kryptering (TDE)</span><span class="sxs-lookup"><span data-stu-id="e17a9-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e17a9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e17a9-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e17a9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e17a9-105">DESCRIPTION</span></span>
<span data-ttu-id="e17a9-106">Get-AzureRmSqlServerTransparentDataEncryptionProtector-cmdleten hämtar information om TDE-skydd.</span><span class="sxs-lookup"><span data-stu-id="e17a9-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="e17a9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e17a9-107">EXAMPLES</span></span>

### <span data-ttu-id="e17a9-108">Exempel 1: Hämta det transparenta data krypterings skyddet (TDE)</span><span class="sxs-lookup"><span data-stu-id="e17a9-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="e17a9-109">Det här kommandot får TDE-skyddet för servern som heter ContosoServer i resurs gruppen med namnet ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e17a9-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="e17a9-110">ResourceGroupName ServerName ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="e17a9-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="e17a9-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="e17a9-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="e17a9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e17a9-112">PARAMETERS</span></span>

### <span data-ttu-id="e17a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e17a9-113">-DefaultProfile</span></span>
<span data-ttu-id="e17a9-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e17a9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e17a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e17a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="e17a9-116">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e17a9-116">The name of the resource group</span></span>

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

### <span data-ttu-id="e17a9-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e17a9-117">-ServerName</span></span>
<span data-ttu-id="e17a9-118">Namnet på Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="e17a9-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="e17a9-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e17a9-119">-Confirm</span></span>
<span data-ttu-id="e17a9-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e17a9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17a9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e17a9-121">-WhatIf</span></span>
<span data-ttu-id="e17a9-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e17a9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e17a9-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e17a9-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e17a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e17a9-124">CommonParameters</span></span>
<span data-ttu-id="e17a9-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e17a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e17a9-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e17a9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e17a9-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e17a9-127">INPUTS</span></span>

### <span data-ttu-id="e17a9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e17a9-128">System.String</span></span>

## <span data-ttu-id="e17a9-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e17a9-129">OUTPUTS</span></span>

### <span data-ttu-id="e17a9-130">Microsoft. Azure. commands. SQL. TransparentDataEncryption. Model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="e17a9-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="e17a9-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e17a9-131">NOTES</span></span>

## <span data-ttu-id="e17a9-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e17a9-132">RELATED LINKS</span></span>

[<span data-ttu-id="e17a9-133">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e17a9-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
