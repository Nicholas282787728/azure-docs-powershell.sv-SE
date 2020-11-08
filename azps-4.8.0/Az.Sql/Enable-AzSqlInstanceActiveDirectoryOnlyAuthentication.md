---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstanceactivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: 16390d5100892c3fcbc2607e55a33bdce9385579
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258567"
---
# <span data-ttu-id="4f63b-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4f63b-101">Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="4f63b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f63b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f63b-103">Möjliggör Azure AD-Only-inloggningsautentisering för en specifik SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="4f63b-103">Enables Azure AD only authentication for a specific SQL Managed Instance.</span></span>

## <span data-ttu-id="4f63b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f63b-104">SYNTAX</span></span>

### <span data-ttu-id="4f63b-105">UseResourceGroupAndInstanceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4f63b-105">UseResourceGroupAndInstanceNameParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f63b-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f63b-106">UseInputObjectParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -InputObject <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f63b-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f63b-107">UserResourceIdParameterSet</span></span>
```
Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f63b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f63b-108">DESCRIPTION</span></span>
<span data-ttu-id="4f63b-109">Cmdleten **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** aktiverar Azure Active Directory (Azure AD) autentiseringskrav endast för en AzureSQL-hanterad instans i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="4f63b-109">The **Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication** cmdlet enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance in the current subscription.</span></span>

## <span data-ttu-id="4f63b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f63b-110">EXAMPLES</span></span>

### <span data-ttu-id="4f63b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4f63b-111">Example 1</span></span>
```powershell
PS C:\>Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01"
ResourceGroupName InstanceName        AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   ManagedInstance01   True
```

<span data-ttu-id="4f63b-112">Det här kommandot aktiverar endast Azure Active Directory (Azure AD) autentiseringskrav för en AzureSQL-hanterad instans som heter ManagedInstance01 som är kopplad till en resurs grupp med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="4f63b-112">This command enables Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Managed Instance named ManagedInstance01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="4f63b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f63b-113">PARAMETERS</span></span>

### <span data-ttu-id="4f63b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f63b-114">-DefaultProfile</span></span>
<span data-ttu-id="4f63b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f63b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f63b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f63b-116">-InputObject</span></span>
<span data-ttu-id="4f63b-117">Det hanterade instans objekt som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4f63b-117">The managed instance object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f63b-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4f63b-118">-InstanceName</span></span>
<span data-ttu-id="4f63b-119">Namnet på den hanterade Azure SQL-instansen Azure Active Directory-inloggningen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="4f63b-119">The name of the Azure SQL Managed Instance the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f63b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f63b-120">-ResourceGroupName</span></span>
<span data-ttu-id="4f63b-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4f63b-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndInstanceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f63b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f63b-122">-ResourceId</span></span>
<span data-ttu-id="4f63b-123">ID för den instans som ska användas</span><span class="sxs-lookup"><span data-stu-id="4f63b-123">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f63b-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f63b-124">-Confirm</span></span>
<span data-ttu-id="4f63b-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f63b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f63b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f63b-126">-WhatIf</span></span>
<span data-ttu-id="4f63b-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f63b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f63b-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f63b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f63b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f63b-129">CommonParameters</span></span>
<span data-ttu-id="4f63b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f63b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f63b-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f63b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f63b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f63b-132">INPUTS</span></span>

### <span data-ttu-id="4f63b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4f63b-133">System.String</span></span>

## <span data-ttu-id="4f63b-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f63b-134">OUTPUTS</span></span>

### <span data-ttu-id="4f63b-135">Microsoft. Azure. commands. SQL. InstanceActiveDirectoryOnlyAuthentication. Model. AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="4f63b-135">Microsoft.Azure.Commands.Sql.InstanceActiveDirectoryOnlyAuthentication.Model.AzureSqlInstanceActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="4f63b-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f63b-136">NOTES</span></span>

## <span data-ttu-id="4f63b-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f63b-137">RELATED LINKS</span></span>

[<span data-ttu-id="4f63b-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4f63b-138">Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="4f63b-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="4f63b-139">Get-AzSqlInstanceActiveDirectoryOnlyAuthentication</span></span>](./Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="4f63b-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4f63b-140">Set-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Set-AzSqlInstanceActiveDirectoryAdministrator.md)

[<span data-ttu-id="4f63b-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4f63b-141">Get-AzSqlInstanceActiveDirectoryAdministrator</span></span>](./Get-AzSqlInstanceActiveDirectoryAdministrator.md)